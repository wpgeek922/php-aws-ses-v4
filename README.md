# php-aws-ses-v4
Amazon Simple Email Service PHP class updated with Signing AWS Requests with Signature Version 4 Support

# Original Class 
 Amazon SimpleEmailService PHP class
 @link http://sourceforge.net/projects/php-aws-ses/
 version 0.8.2

# Usage
```
 require_once("ses.php");
    
 $ses = new SimpleEmailService("AWS_ACCESS_KEY", 
 "AWS_SECRET_KEY", "AWS_REGION");

 $msg = new SimpleEmailServiceMessage();

 $msg->from = "awesomeguy@exampledomain.com";
 $msg->subject = "Update V4 Signature";
 $msg->messagetext = "Amazon SES PHP Class With V4 Signature";
 $msg->to = array("someotherawesomeguy@exampledomain.com");

 try {
  $res = $ses->sendEmail($msg);
  var_dump($res);
 } catch (Exception $e) {
  var_dump($e);
 }
```
