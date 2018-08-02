---
UID: NS:wlanapi._WLAN_CONNECTION_NOTIFICATION_DATA
title: "_WLAN_CONNECTION_NOTIFICATION_DATA"
author: windows-sdk-content
description: Contains information about connection related notifications.
old-location: nwifi\wlan_connection_notification_data.htm
old-project: NativeWiFi
ms.assetid: 005af5ef-994d-425a-be4b-54567a733fb3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PWLAN_CONNECTION_NOTIFICATION_DATA, PWLAN_CONNECTION_NOTIFICATION_DATA, PWLAN_CONNECTION_NOTIFICATION_DATA structure pointer [NativeWIFI], WLAN_CONNECTION_NOTIFICATION_ADHOC_NETWORK_FORMED, WLAN_CONNECTION_NOTIFICATION_CONSOLE_USER_PROFILE, WLAN_CONNECTION_NOTIFICATION_DATA, WLAN_CONNECTION_NOTIFICATION_DATA structure [NativeWIFI], _WLAN_CONNECTION_NOTIFICATION_DATA, nwifi.wlan_connection_notification_data, wlanapi/PWLAN_CONNECTION_NOTIFICATION_DATA, wlanapi/WLAN_CONNECTION_NOTIFICATION_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WLAN_CONNECTION_NOTIFICATION_DATA, *PWLAN_CONNECTION_NOTIFICATION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_CONNECTION_NOTIFICATION_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_CONNECTION_NOTIFICATION_DATA structure


## -description


The <b>WLAN_CONNECTION_NOTIFICATION_DATA</b> structure contains information about connection related notifications.


## -struct-fields




### -field wlanConnectionMode

A <a href="https://msdn.microsoft.com/d62e863f-2aa8-49b1-9e27-8d9d053026f0">WLAN_CONNECTION_MODE</a> value that specifies the mode of the connection.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_connection_mode_profile</b>  value is supported.


### -field strProfileName

The name of the profile used for the connection. WLAN_MAX_NAME_LENGTH is 256. Profile names are case-sensitive. This string must be NULL-terminated.


### -field dot11Ssid

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548773">DOT11_SSID</a> structure that contains the SSID of the association.


### -field dot11BssType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547669">DOT11_BSS_TYPE</a> value that indicates the BSS network type.


### -field bSecurityEnabled

Indicates whether security is enabled for this connection.  If <b>TRUE</b>, security is enabled.  


### -field wlanReasonCode

A <a href="https://msdn.microsoft.com/7b267f0b-b3f7-4729-bab4-de3bdd0a35a2">WLAN_REASON_CODE</a> that indicates the reason for an operation failure.  This field has a value of <b>WLAN_REASON_CODE_SUCCESS</b> for all connection-related notifications except <b>wlan_notification_acm_connection_complete</b>.  If the connection fails, this field indicates the reason for the failure.


### -field dwFlags

A set of flags that provide additional information for the network connection.  

This member can be one of the following values defined in the <i>Wlanapi.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLAN_CONNECTION_NOTIFICATION_ADHOC_NETWORK_FORMED"></a><a id="wlan_connection_notification_adhoc_network_formed"></a><dl>
<dt><b>WLAN_CONNECTION_NOTIFICATION_ADHOC_NETWORK_FORMED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that an adhoc network is formed.

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_CONNECTION_NOTIFICATION_CONSOLE_USER_PROFILE"></a><a id="wlan_connection_notification_console_user_profile"></a><dl>
<dt><b>WLAN_CONNECTION_NOTIFICATION_CONSOLE_USER_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the connection uses a per-user profile owned by the console user. Non-console users will not be able to see the profile in their profile list.

</td>
</tr>
</table>
 


### -field strProfileXml

This field contains the XML presentation of the profile used for discovery, if the connection succeeds.


## -remarks



The <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. 

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_ACM</b>, then the received notification is an auto configuration module notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure.  For some of these notifications, a <b>WLAN_CONNECTION_NOTIFICATION_DATA</b> structure is returned in the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure. 

For more information on these notifications, see the <a href="https://msdn.microsoft.com/b0814b2a-ccdc-4bf1-b11e-25f2cf6ba9bd">WLAN_NOTIFICATION_ACM</a> enumeration reference.




## -see-also




<a href="https://msdn.microsoft.com/b0814b2a-ccdc-4bf1-b11e-25f2cf6ba9bd">WLAN_NOTIFICATION_ACM</a>



<a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

