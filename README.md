# XLRelease

A [Logscape][reference-logscape] App for monitoring XL Release.

This will ensure your XL Release Logs are properly ingested into Logscape. 

## Installation Steps
1. Download the latest release as a Zip.
2. Deploy to your logscape environment
3. Go to your Data Sources page and check that your log locations are included. If not, update them.

By default, we have set D:\XLRelease. As needed, please update the xlreleaseapp_datasources.config with extra paths that should be included. 

## Audit Logging
By default, XL Release does not log out it's Audit trail. Technically you can get most of the detail from the xl-release log but the Audit.log is cleaner - so I'd recommend you use it. For more informtion, check out the [XL Release Logging guide][reference-xlrlogging]
  1. Go to your XL Release Home Directory
  2. Open up /conf/logback.xml
  3. Turn the Audit logger to Info

If you amend the location of any of the logs in the logback.xml file, make sure you update your Logscape data sources

### Next Steps
So far we have only a few searches and workspaces. Next probable steps:

1. Alerts on Failure - Whilst XLR provides Alerts to Template owners, the XLR Support Team may not necessarily be on the recieving end. 
2. Daily Reports - Actions taken by uses, most amended templates etc
3. Auditing Pages - Tracking the updates

[reference-logscape]: http://logscape.com/
[reference-xlrlogging]: https://docs.xebialabs.com/xl-release/concept/logging-in-xl-release.html
