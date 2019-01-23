---
UID: NE:wlanapi._WLAN_HOSTED_NETWORK_NOTIFICATION_CODE
title: WLAN_HOSTED_NETWORK_NOTIFICATION_CODE
author: windows-sdk-content
description: Specifies the possible values of the NotificationCode parameter for received notifications on the wireless Hosted Network.
old-location: nwifi\wlan_hosted_network_notification_code.htm
tech.root: NativeWiFi
ms.assetid: f01e4a42-3378-4ceb-b23b-5deb78fb18ca
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_NOTIFICATION_CODE, PWLAN_HOSTED_NETWORK_NOTIFICATION_CODE, PWLAN_HOSTED_NETWORK_NOTIFICATION_CODE enumeration pointer [NativeWIFI], WLAN_HOSTED_NETWORK_NOTIFICATION_CODE, WLAN_HOSTED_NETWORK_NOTIFICATION_CODE enumeration [NativeWIFI], nwifi.wlan_hosted_network_notification_code, wlan_hosted_network_peer_state_change, wlan_hosted_network_radio_state_change, wlan_hosted_network_state_change, wlanapi/PWLAN_HOSTED_NETWORK_NOTIFICATION_CODE, wlanapi/WLAN_HOSTED_NETWORK_NOTIFICATION_CODE, wlanapi/wlan_hosted_network_peer_state_change, wlanapi/wlan_hosted_network_radio_state_change, wlanapi/wlan_hosted_network_state_change"
ms.topic: enum
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_NOTIFICATION_CODE
product: Windows
targetos: Windows
req.typenames: WLAN_HOSTED_NETWORK_NOTIFICATION_CODE, *PWLAN_HOSTED_NETWORK_NOTIFICATION_CODE
req.redist: 
---

# WLAN_HOSTED_NETWORK_NOTIFICATION_CODE enumeration


## -description


The <b>WLAN_HOSTED_NETWORK_NOTIFICATION_CODE</b> enumerated type specifies the possible values of the NotificationCode parameter for received notifications on the wireless Hosted Network.


## -enum-fields




### -field wlan_hosted_network_state_change

The Hosted Network state has changed.


### -field wlan_hosted_network_peer_state_change

The Hosted Network peer state has changed.


### -field wlan_hosted_network_radio_state_change

The Hosted Network radio state has changed.


### -field v1_enum




## -remarks



The <b>WLAN_HOSTED_NETWORK_NOTIFICATION_CODE</b> enumerated type is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  on Windows Server 2008 R2 with the Wireless LAN Service installed.  

The <b>WLAN_HOSTED_NETWORK_NOTIFICATION_CODE</b> specifies the possible values for the NotificationCode parameter for received notifications  when the NotificationSource parameter is WLAN_NOTIFICATION_SOURCE_HNWK on the wireless Hosted Network. 

The starting value for the <b>WLAN_HOSTED_NETWORK_NOTIFICATION_CODE</b> enumeration is defined as L2_NOTIFICATION_CODE_V2_BEGIN, which is defined  in the <i>l2cmn.h</i> header file.  Note that the <i>l2cmn.h</i> header is automatically included by the <i>wlanapi.h</i> header file.



The <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_HNWK</b>, then the received notification is a wireless Hosted Network notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure. 




<table>
<tr>
<th><b>NotificationCode</b></th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_state_change"></a><a id="WLAN_HOSTED_NETWORK_STATE_CHANGE"></a>wlan_hosted_network_state_change

</td>
<td width="60%">
The <i>pData</i> member of <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure  should be cast to a pointer to a <a href="https://msdn.microsoft.com/e05607fd-da1e-49ae-b2eb-3ac4758df84c">WLAN_HOSTED_NETWORK_STATE_CHANGE</a> structure and <b>dwDataSize</b> member  would be at least as large as sizeof(<b>WLAN_HOSTED_NETWORK_STATE_CHANGE</b>). 

</td>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_peer_state_change"></a><a id="WLAN_HOSTED_NETWORK_PEER_STATE_CHANGE"></a>wlan_hosted_network_peer_state_change

</td>
<td width="60%">
the <i>pData</i> member of <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure  should be cast to a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd439500(v=VS.85).aspx">WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</a> structure and <b>dwDataSize</b> member  would be at least as large as sizeof(<b>WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</b>). 

</td>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_radio_state_change"></a><a id="WLAN_HOSTED_NETWORK_RADIO_STATE_CHANGE"></a>wlan_hosted_network_radio_state_change

</td>
<td width="60%">
the <i>pData</i> member of <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure  should be cast to a pointer to a <a href="https://msdn.microsoft.com/a84db78d-f6fd-48c4-80e8-a0d16f4dc3ed">WLAN_HOSTED_NETWORK_RADIO_STATE</a>  structure and <b>dwDataSize</b> member  would be at least as large as sizeof(<b>WLAN_HOSTED_NETWORK_RADIO_STATE</b> ). 

</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd439500(v=VS.85).aspx">WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</a>



<a href="https://msdn.microsoft.com/a84db78d-f6fd-48c4-80e8-a0d16f4dc3ed">WLAN_HOSTED_NETWORK_RADIO_STATE</a>



<a href="https://msdn.microsoft.com/e05607fd-da1e-49ae-b2eb-3ac4758df84c">WLAN_HOSTED_NETWORK_STATE_CHANGE</a>



<a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

