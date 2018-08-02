---
UID: NE:wlanapi._WLAN_NOTIFICATION_MSM
title: "_WLAN_NOTIFICATION_MSM"
author: windows-sdk-content
description: Specifies the possible values of the NotificationCode member of the WLAN_NOTIFICATION_DATA structure for Media Specific Module (MSM) notifications.
old-location: nwifi\wlan_notification_msm.htm
old-project: NativeWiFi
ms.assetid: 7847658a-6789-43ad-95ad-b520333863e6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PWLAN_NOTIFICATION_MSM, PWLAN_NOTIFICATION_MSM, PWLAN_NOTIFICATION_MSM enumeration pointer [NativeWIFI], WLAN_NOTIFICATION_MSM, WLAN_NOTIFICATION_MSM enumeration [NativeWIFI], _WLAN_NOTIFICATION_MSM, nwifi.wlan_notification_msm, wlan_notification_msm_adapter_operation_mode_change, wlan_notification_msm_adapter_removal, wlan_notification_msm_associated, wlan_notification_msm_associating, wlan_notification_msm_authenticating, wlan_notification_msm_connected, wlan_notification_msm_disassociating, wlan_notification_msm_disconnected, wlan_notification_msm_end, wlan_notification_msm_peer_join, wlan_notification_msm_peer_leave, wlan_notification_msm_radio_state_change, wlan_notification_msm_roaming_end, wlan_notification_msm_roaming_start, wlan_notification_msm_signal_quality_change, wlan_notification_msm_start, wlanapi/PWLAN_NOTIFICATION_MSM, wlanapi/WLAN_NOTIFICATION_MSM, wlanapi/wlan_notification_msm_adapter_operation_mode_change, wlanapi/wlan_notification_msm_adapter_removal, wlanapi/wlan_notification_msm_associated, wlanapi/wlan_notification_msm_associating, wlanapi/wlan_notification_msm_authenticating, wlanapi/wlan_notification_msm_connected, wlanapi/wlan_notification_msm_disassociating, wlanapi/wlan_notification_msm_disconnected, wlanapi/wlan_notification_msm_end, wlanapi/wlan_notification_msm_peer_join, wlanapi/wlan_notification_msm_peer_leave, wlanapi/wlan_notification_msm_radio_state_change, wlanapi/wlan_notification_msm_roaming_end, wlanapi/wlan_notification_msm_roaming_start, wlanapi/wlan_notification_msm_signal_quality_change, wlanapi/wlan_notification_msm_start"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: WLAN_NOTIFICATION_MSM, *PWLAN_NOTIFICATION_MSM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_NOTIFICATION_MSM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_NOTIFICATION_MSM enumeration


## -description


The <b>WLAN_NOTIFICATION_MSM</b> enumerated type specifies the possible values of the <b>NotificationCode</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure for Media Specific Module  (MSM) notifications.


## -enum-fields




### -field wlan_notification_msm_start

The beginning of the range that specifies the possible values for ACM notifications.


### -field wlan_notification_msm_associating

A wireless device is in the process of associating with an access point or a peer station. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_associated

The wireless device has associated with an access point or a peer station.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_authenticating

The wireless device is in the process of authenticating.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_connected

The wireless device is associated with an access point or a peer station, keys have been exchanged, and the wireless device is available to send data. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_roaming_start

The wireless device is connected to an access point and has initiated roaming to another access point.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_roaming_end

The wireless device was connected to an access point and has completed roaming to another access point.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_radio_state_change

The radio state for an adapter has changed. Each physical layer (PHY) has its own radio state. The radio for an adapter is switched off when the radio state of every PHY is off.  

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a <a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a> structure that identifies the new radio state.


### -field wlan_notification_msm_signal_quality_change

A signal quality change for the currently associated access point or peer station.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a ULONG WLAN_SIGNAL_QUALITY that identifies  the new signal quality.


### -field wlan_notification_msm_disassociating

A wireless device is in the process of disassociating from an access point or a peer station. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information. 


### -field wlan_notification_msm_disconnected

The wireless device is not associated with an access point or a peer station. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information. The <b>wlanReasonCode</b> member of the <b>WLAN_MSM_NOTIFICATION_DATA</b> structure  indicates the reason for the disconnect.


### -field wlan_notification_msm_peer_join

A peer has joined an adhoc network.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_peer_leave

A peer has left an adhoc network.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.


### -field wlan_notification_msm_adapter_removal

A wireless adapter has been removed from the local computer. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information. 


### -field wlan_notification_msm_adapter_operation_mode_change

The operation mode of the wireless device has changed. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a ULONG that identifies the new operation mode.


### -field wlan_notification_msm_link_degraded


### -field wlan_notification_msm_link_improved


### -field wlan_notification_msm_end

Indicates the end of the range that specifies the possible values for MSM notifications.


### -field v1_enum




## -remarks



The <a href="https://msdn.microsoft.com/b0814b2a-ccdc-4bf1-b11e-25f2cf6ba9bd">WLAN_NOTIFICATION_ACM</a> enumerated type is used by the Media Specific Module, the new wireless configuration component supported on Windows Vista and  later.  

The <b>WLAN_NOTIFICATION_MSM</b> specifies the possible values for the <b>NotificationCode</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure for received notifications  when the <b>NotificationSource</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure is <b>WLAN_NOTIFICATION_SOURCE_MSM</b>. 

The starting value for the <b>WLAN_NOTIFICATION_MSM</b> enumeration is defined as L2_NOTIFICATION_CODE_PUBLIC_BEGIN in the <i>l2cmn.h</i> header file.  Note that the <i>l2cmn.h</i> header is automatically included by the <i>wlanapi.h</i> header file.



The <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/76693a8e-7df8-45f0-a3c1-7960de27250c">WLAN_MSM_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

