# jwplayer

url : http://developer.jwplayer.com/jw-platform/reference/v1/index.html

An server side API for implementation of jwplayer uplaoad function.
It is an conversion of php API.

----------------------------------------------------------------------------

Usage : 

var jwplayer = require('jwplayer');

/**
   *  jwplayer api used to generate api key and upload file
   *  json response 
   *  @Dependency : jwplayer 
   *
  */
createKey: function (req, res) {
    var arguments = {'resumable': 'False'};
    jwplayer.setArguments(arguments, function(error, response, body) {
      if(error) {
        res.send(error);
      } else {
        res.send(body);
      }
    });
  },

