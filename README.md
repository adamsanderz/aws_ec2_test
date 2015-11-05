## Synopsis

This project is to help demonstrate a 403 Forbidden response when attempting to call describeInstances() from within an Ionic app on either an Android or iOS device.  This same application, when run from a desktop browser, works and returns the expected results. 

## Code Example

You will need to provide your own **accessKeyId** and **secretAccessKey** (www/index.html) associate to an IAM that has the following policy assocated.

```javascript
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Stmt1443789530000",
            "Effect": "Allow",
            "Action": [
                "ec2:StartInstances",
                "ec2:StopInstances",
                "ec2:Describe*"
            ],
            "Resource": [
                "*"
            ]
        }
    ]
}
```

## Motivation

See Synopsis above

## Installation

It is recommended that you have an Ionic environment with either Android or IOS platform support installed.

## Tests

To see the example app work run 'ionic serve'. To see the 403 Forbidden response from Amazon run 'ionic run android' (Android device must be connected to computer) or 'ionic run ios' (iOS device must be connected to computer).  Else you can recreate the 403 Forbidden response in the associated emulators 'ionic emulate android' or 'ionic emulate ios'.
