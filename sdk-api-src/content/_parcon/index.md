---
UID: TP:parcon
ms.assetid: d41c225a-7794-30c9-9b0b-8612948bb42f
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Parental Controls



Overview of the Parental Controls technology.

To develop Parental Controls, you need these headers:

 * [wpcapi.h](..\wpcapi\index.md)
 * [wpcevent.h](..\wpcevent\index.md)

For the programming guide, see [Parental Controls](https://review.docs.microsoft.com/en-us/win32-test/parcon).

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [tagWPCFLAG_IM_FEATURE enumeration](..\wpcevent\ne-wpcevent-tagwpcflag_im_feature.md) | Indicates information about the features accessed during an instant messaging interaction. |
| [tagWPCFLAG_IM_LEAVE_FLAG enumeration](..\wpcevent\ne-wpcevent-tagwpcflag_im_leave_flag.md) | Indicates information about when a participant leaves the instant messaging interaction. |
| [tagWPCFLAG_ISBLOCKED enumeration](..\wpcevent\ne-wpcevent-tagwpcflag_isblocked.md) | Indicates information about what events are blocked from use and what controls are in place. |
| [tagWPCFLAG_LOGOFF_TYPE enumeration](..\wpcevent\ne-wpcevent-tagwpcflag_logoff_type.md) | Indicates information about the type of logoff method used. |
| [tagWPC_ARGS_CONVERSATIONINITEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_conversationinitevent.md) | Indicates information about initiating a conversation. |
| [tagWPC_ARGS_CONVERSATIONJOINEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_conversationjoinevent.md) | Indicates information about joining an existing conversation. |
| [tagWPC_ARGS_CONVERSATIONLEAVEEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_conversationleaveevent.md) | Indicates information about leaving a conversation. |
| [tagWPC_ARGS_CUSTOMEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_customevent.md) | Indicates information about a user-defined event that is not covered by the general events. |
| [tagWPC_ARGS_EMAILCONTACTEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_emailcontactevent.md) | Indicates information about contacting someone by using email. |
| [tagWPC_ARGS_EMAILRECEIEVEDEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_emailreceievedevent.md) | Indicates information about an email message that has been received. |
| [tagWPC_ARGS_EMAILSENTEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_emailsentevent.md) | Indicates information about an email message that has been sent. |
| [tagWPC_ARGS_FILEDOWNLOADEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_filedownloadevent.md) | Indicates information about a file that has been downloaded. |
| [tagWPC_ARGS_GAMESTARTEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_gamestartevent.md) | Indicates information about the start of a computer game. |
| [tagWPC_ARGS_IMCONTACTEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_imcontactevent.md) | Indicates information about contacting someone by using an instant messaging application. |
| [tagWPC_ARGS_IMFEATUREEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_imfeatureevent.md) | Indicates information about the features of the instant messaging interaction. |
| [tagWPC_ARGS_MEDIADOWNLOADEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_mediadownloadevent.md) | Indicates information about the download of a media file. |
| [tagWPC_ARGS_MEDIAPLAYBACKEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_mediaplaybackevent.md) | Indicates information about the playback of a media file. |
| [tagWPC_ARGS_SAFERAPPBLOCKED enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_saferappblocked.md) | Indicates information about a safer application that is being blocked. |
| [tagWPC_ARGS_SETTINGSCHANGEEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_settingschangeevent.md) | Indicates information about the changes to settings being made by a user. |
| [tagWPC_ARGS_URLVISITEVENT enumeration](..\wpcevent\ne-wpcevent-tagwpc_args_urlvisitevent.md) | Indicates information about the address URL of a website viewed. |
| [tagWPC_MEDIA_EXPLICIT_TYPE enumeration](..\wpcevent\ne-wpcevent-tagwpc_media_explicit_type.md) | Indicates information about the explicit rating of the media file. |
| [tagWPC_MEDIA_TYPE enumeration](..\wpcevent\ne-wpcevent-tagwpc_media_type.md) | Indicates information about the type of media file accessed. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IWPCGamesSettings interface](..\wpcapi\nn-wpcapi-iwpcgamessettings.md) | Accesses games settings for the user. |
| [IWPCProviderConfig interface](..\wpcapi\nn-wpcapi-iwpcproviderconfig.md) | Exposes configuration methods that are implemented by third parties. |
| [IWPCProviderState interface](..\wpcapi\nn-wpcapi-iwpcproviderstate.md) | Exposes provider state methods that are implemented by third parties. |
| [IWPCProviderSupport interface](..\wpcapi\nn-wpcapi-iwpcprovidersupport.md) | Exposes methods that allow third-party providers to query the currently enabled provider. |
| [IWPCSettings interface](..\wpcapi\nn-wpcapi-iwpcsettings.md) | Accesses general settings for the user. |
| [IWPCWebSettings interface](..\wpcapi\nn-wpcapi-iwpcwebsettings.md) | Accesses web restrictions settings for the user. |
| [IWindowsParentalControls interface](..\wpcapi\nn-wpcapi-iwindowsparentalcontrols.md) | Enables access to all settings interfaces of the Minimum Compliance API. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IWPCGamesSettings::IsBlocked](..\wpcapi\nf-wpcapi-iwpcgamessettings-isblocked.md) | Determines whether the specified game is blocked from execution. |
| [IWPCProviderConfig::Configure](..\wpcapi\nf-wpcapi-iwpcproviderconfig-configure.md) | Called for the current provider when you click a user tile in the Parental Controls Control Panel. This method allows for changes to the configuration. |
| [IWPCProviderConfig::GetUserSummary](..\wpcapi\nf-wpcapi-iwpcproviderconfig-getusersummary.md) | Retrieves the information for each user by using the Parental Controls Control Panel. |
| [IWPCProviderConfig::RequestOverride](..\wpcapi\nf-wpcapi-iwpcproviderconfig-requestoverride.md) | Called for the current provider to enable configuration override. |
| [IWPCProviderState::Disable](..\wpcapi\nf-wpcapi-iwpcproviderstate-disable.md) | Notifies the third-party application that it is not the current provider. |
| [IWPCProviderState::Enable](..\wpcapi\nf-wpcapi-iwpcproviderstate-enable.md) | Notifies the third-party application that it has been selected as the new current provider. |
| [IWPCProviderSupport::GetCurrent](..\wpcapi\nf-wpcapi-iwpcprovidersupport-getcurrent.md) | Retrieves the GUID of the current provider. |
| [IWPCSettings::GetLastSettingsChangeTime](..\wpcapi\nf-wpcapi-iwpcsettings-getlastsettingschangetime.md) | Retrieves the time at which the configuration settings were last updated. |
| [IWPCSettings::GetRestrictions](..\wpcapi\nf-wpcapi-iwpcsettings-getrestrictions.md) | Determines whether web restrictions, time limits, or game restrictions are on. |
| [IWPCSettings::IsLoggingRequired](..\wpcapi\nf-wpcapi-iwpcsettings-isloggingrequired.md) | Determines whether activity logging should be performed when obtaining the IWPCSettings interface. |
| [IWPCWebSettings::GetSettings](..\wpcapi\nf-wpcapi-iwpcwebsettings-getsettings.md) | Retrieves the web restrictions settings. |
| [IWPCWebSettings::RequestURLOverride](..\wpcapi\nf-wpcapi-iwpcwebsettings-requesturloverride.md) | Requests that the Parental Controls web restrictions subsystem set the specified primary and sub URLs to the allowed state. |
| [IWindowsParentalControls::GetGamesSettings](..\wpcapi\nf-wpcapi-iwindowsparentalcontrols-getgamessettings.md) | Retrieves a pointer to an interface for games restrictions settings for the specified user. |
