# spo cdn origin remove

Removes CDN origin for the current SharePoint Online tenant

## Usage

```sh
spo cdn origin remove [options]
```

## Options

Option|Description
------|-----------
`--help`|output usage information
`-t, --type [type]`|Type of CDN to manage. `Public|Private`. Default `Public`
`-r, --origin <origin>`|Origin to remove from the current CDN configuration
`--confirm`|Don't prompt for confirming removal of a tenant property
`-o, --output [output]`|Output type. `json|text`. Default `text`
`--verbose`|Runs command with verbose logging
`--debug`|Runs command with debug logging

!!! important
    Before using this command, log in to a SharePoint Online tenant admin site, using the [spo login](../login.md) command.

## Remarks

To remove an origin from an Office 365 CDN, you have to first log in to a tenant admin site using the [spo login](../login.md) command, eg. `spo login https://contoso-admin.sharepoint.com`. If you are logged in to a different site and will try to manage tenant properties, you will get an error.

Using the `-t, --type` option you can choose whether you want to manage the settings of the Public (default) or Private CDN. If you don't use the option, the command will use the Public CDN.

## Examples

Remove _*/CDN_ from the list of origins of the Public CDN

```sh
spo cdn origin remove -t Public -r */CDN
```

## More information

- General availability of Office 365 CDN: [https://dev.office.com/blogs/general-availability-of-office-365-cdn](https://dev.office.com/blogs/general-availability-of-office-365-cdn)
