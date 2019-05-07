# ![LOGO](logo.png) ManagementLinkClient **flow**ground Connector

## Description

A generated **flow**ground connector for the ManagementLinkClient API (version 2016-09-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/resources-links/2016-09-01/swagger.json<br/>
Generated at: 2019-05-07T17:38:45+03:00

## API Description

Azure resources can be linked together to form logical relationships. You can establish links between resources belonging to different resource groups. However, all the linked resources must belong to the same subscription. Each resource can be linked to 50 other resources. If any of the linked resources are deleted or moved, the link owner must clean up the remaining link.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists all of the available Microsoft.Resources REST API operations.

*Tags:* `Operations`

#### Input Parameters
* `api-version` - _required_ - The API version to use for the operation.

### Gets all the linked resources for the subscription.

*Tags:* `ResourceLinks`

#### Input Parameters
* `$filter` - _optional_ - The filter to apply on the list resource links operation. The supported filter for list resource links is targetId. For example, $filter=targetId eq {value}
* `api-version` - _required_ - The API version to use for the operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Deletes a resource link with the specified ID.

*Tags:* `ResourceLinks`

#### Input Parameters
* `linkId` - _required_ - The fully qualified ID of the resource link. Use the format, /subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/{provider-namespace}/{resource-type}/{resource-name}/Microsoft.Resources/links/{link-name}. For example, /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myGroup/Microsoft.Web/sites/mySite/Microsoft.Resources/links/myLink
* `api-version` - _required_ - The API version to use for the operation.

### Gets a resource link with the specified ID.

*Tags:* `ResourceLinks`

#### Input Parameters
* `linkId` - _required_ - The fully qualified Id of the resource link. For example, /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myGroup/Microsoft.Web/sites/mySite/Microsoft.Resources/links/myLink
* `api-version` - _required_ - The API version to use for the operation.

### Creates or updates a resource link between the specified resources.

*Tags:* `ResourceLinks`

#### Input Parameters
* `linkId` - _required_ - The fully qualified ID of the resource link. Use the format, /subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/{provider-namespace}/{resource-type}/{resource-name}/Microsoft.Resources/links/{link-name}. For example, /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myGroup/Microsoft.Web/sites/mySite/Microsoft.Resources/links/myLink
* `api-version` - _required_ - The API version to use for the operation.

### Gets a list of resource links at and below the specified source scope.

*Tags:* `ResourceLinks`

#### Input Parameters
* `scope` - _required_ - The fully qualified ID of the scope for getting the resource links. For example, to list resource links at and under a resource group, set the scope to /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myGroup.
* `$filter` - _optional_ - The filter to apply when getting resource links. To get links only at the specified scope (not below the scope), use Filter.atScope().
    Possible values: atScope().
* `api-version` - _required_ - The API version to use for the operation.

## License

**flow**ground :- Telekom iPaaS / azure-com-resources-links-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
