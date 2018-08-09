---
UID: NS:wlanapi._WLAN_MSM_NOTIFICATION_DATA
title: "_WLAN_MSM_NOTIFICATION_DATA"
author: windows-sdk-content
description: Contains information about media specific module (MSM) connection related notifications.
old-location: nwifi\wlan_msm_notification_data.htm
old-project: nativewifi
ms.assetid: 76693a8e-7df8-45f0-a3c1-7960de27250c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PWLAN_MSM_NOTIFICATION_DATA, PWLAN_MSM_NOTIFICATION_DATA, PWLAN_MSM_NOTIFICATION_DATA structure pointer [NativeWIFI], WLAN_MSM_NOTIFICATION_DATA, WLAN_MSM_NOTIFICATION_DATA structure [NativeWIFI], _WLAN_MSM_NOTIFICATION_DATA, nwifi.wlan_msm_notification_data, wlanapi/PWLAN_MSM_NOTIFICATION_DATA, wlanapi/WLAN_MSM_NOTIFICATION_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: WLAN_MSM_NOTIFICATION_DATA, *PWLAN_MSM_NOTIFICATION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_MSM_NOTIFICATION_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_MSM_NOTIFICATION_DATA structure


## -description


The <b>WLAN_MSM_NOTIFICATION_DATA</b> structure contains information about media specific module (MSM) connection related notifications.


## -struct-fields




### -field wlanConnectionMode

A <a href="https://msdn.microsoft.com/d62e863f-2aa8-49b1-9e27-8d9d053026f0">WLAN_CONNECTION_MODE</a> value that specifies the mode of the connection.


### -field strProfileName

The name of the profile used for the connection. WLAN_MAX_NAME_LENGTH is 256. Profile names are case-sensitive. This string must be NULL-terminated.


### -field dot11Ssid

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548773">DOT11_SSID</a> structure that contains the SSID of the association.


### -field dot11BssType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547669">DOT11_BSS_TYPE</a> value that indicates the BSS network type.


### -field dot11MacAddr

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548681">DOT11_MAC_ADDRESS</a> that specifies the MAC address of the peer or access point.


### -field bSecurityEnabled

Indicates whether security is enabled for this connection.  If <b>TRUE</b>, security is enabled.  


### -field bFirstPeer

Indicates whether the peer is the first to join the ad hoc network created by the machine. If <b>TRUE</b>, the peer is the first to join.

After the first peer joins the network, the interface state of the machine that created the ad hoc network changes from wlan_interface_state_ad_hoc_network_formed to wlan_interface_state_connected.


### -field bLastPeer

Indicates whether the peer is the last to leave the ad hoc network created by the machine. If <b>TRUE</b>, the peer is the last to leave. After the last peer leaves the network, the interface state of the machine that created the ad hoc network changes from wlan_interface_state_connected to wlan_interface_state_ad_hoc_network_formed.


### -field wlanReasonCode

A <a href="https://msdn.microsoft.com/7b267f0b-b3f7-4729-bab4-de3bdd0a35a2">WLAN_REASON_CODE</a> that indicates the reason for an operation failure.  If the operation succeeds, this field has a value of <b>WLAN_REASON_CODE_SUCCESS</b>. Otherwise, this field indicates the reason for the failure.


## -remarks



The <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. 

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_MSM</b>, then the received notification is a media specific module (MSM) notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure.  For some of these notifications, a <b>WLAN_MSM_NOTIFICATION_DATA</b> structure is returned in the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure. 

For more information on these notifications, see the <a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a> enumeration reference.




## -see-also




<a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

