---
UID: TP:wcm
ms.assetid: 022e09f2-6845-37d9-bf82-c9eb1f6ba5ab
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Windows Connection Manager



Overview of the Windows Connection Manager technology.

To develop Windows Connection Manager, you need these headers:

 * [wcmapi.h](..\wcmapi\index.md)

For the programming guide, see [Windows Connection Manager](/windows/desktop/wcm).

## Functions

| Title   | Description   |
| ---- |:---- |
| [WcmFreeMemory function](..\wcmapi\nf-wcmapi-wcmfreememory.md) | Is used to release memory resources allocated by the WCM functions. |
| [WcmGetProfileList function](..\wcmapi\nf-wcmapi-wcmgetprofilelist.md) | Retrieves a list of profiles in preferred order. |
| [WcmQueryProperty function](..\wcmapi\nf-wcmapi-wcmqueryproperty.md) | Retrieves the value of a specified WCM property. |
| [WcmSetProfileList function](..\wcmapi\nf-wcmapi-wcmsetprofilelist.md) | Reorders a profile list or a subset of a profile list. |
| [WcmSetProperty function](..\wcmapi\nf-wcmapi-wcmsetproperty.md) | Sets the value of a WCM property. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [WCM_BILLING_CYCLE_INFO structure](..\wcmapi\ns-wcmapi-wcm_billing_cycle_info.md) | Specifies information about the billing cycle. |
| [_WCM_CONNECTION_COST_DATA structure](..\wcmapi\ns-wcmapi-_wcm_connection_cost_data.md) | Specifies information about a connection cost. |
| [_WCM_DATAPLAN_STATUS structure](..\wcmapi\ns-wcmapi-_wcm_dataplan_status.md) | Specifies subscription information for a network connection. |
| [_WCM_POLICY_VALUE structure](..\wcmapi\ns-wcmapi-_wcm_policy_value.md) | Contains information about the current value of a policy. |
| [_WCM_PROFILE_INFO structure](..\wcmapi\ns-wcmapi-_wcm_profile_info.md) | Contains information about a specific profile. |
| [_WCM_PROFILE_INFO_LIST structure](..\wcmapi\ns-wcmapi-_wcm_profile_info_list.md) | Contains a list of profiles in preferred order. |
| [_WCM_TIME_INTERVAL structure](..\wcmapi\ns-wcmapi-_wcm_time_interval.md) | Defines a time interval. |
| [_WCM_USAGE_DATA structure](..\wcmapi\ns-wcmapi-_wcm_usage_data.md) | Contains information related to connection usage. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_WCM_CONNECTION_COST enumeration](..\wcmapi\ne-wcmapi-_wcm_connection_cost.md) | Determines the connection cost type and flags. |
| [_WCM_CONNECTION_COST_SOURCE enumeration](..\wcmapi\ne-wcmapi-_wcm_connection_cost_source.md) | Specifies the source that provides connection cost information. |
| [_WCM_MEDIA_TYPE enumeration](..\wcmapi\ne-wcmapi-_wcm_media_type.md) | Specifies the type of media for a connection. |
| [_WCM_PROPERTY enumeration](..\wcmapi\ne-wcmapi-_wcm_property.md) | Specifies a property of a connection. |
