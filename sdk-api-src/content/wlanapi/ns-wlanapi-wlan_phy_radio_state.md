---
UID: NS:wlanapi._WLAN_PHY_RADIO_STATE
title: WLAN_PHY_RADIO_STATE
author: windows-sdk-content
description: Specifies the radio state.
old-location: nwifi\wlan_phy_radio_state.htm
tech.root: NativeWiFi
ms.assetid: 20da1494-4264-4d0d-b789-25e2be6a8dd4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_PHY_RADIO_STATE, PWLAN_PHY_RADIO_STATE, PWLAN_PHY_RADIO_STATE structure pointer [NativeWIFI], WLAN_PHY_RADIO_STATE, WLAN_PHY_RADIO_STATE structure [NativeWIFI], nwifi.wlan_phy_radio_state, wlanapi/PWLAN_PHY_RADIO_STATE, wlanapi/WLAN_PHY_RADIO_STATE"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_PHY_RADIO_STATE
product: Windows
targetos: Windows
req.typenames: WLAN_PHY_RADIO_STATE, *PWLAN_PHY_RADIO_STATE
req.redist: 
---

# WLAN_PHY_RADIO_STATE structure


## -description


The <b>WLAN_PHY_RADIO_STATE</b> structure specifies the radio state on a specific physical layer (PHY) type.


## -struct-fields




### -field dwPhyIndex

The index of the PHY type on which the radio state is being set or queried. The <a href="https://msdn.microsoft.com/09f8273a-5259-44fa-b55e-af3282735c0b">WlanGetInterfaceCapability</a> function returns a list of valid PHY types.


### -field dot11SoftwareRadioState

A <a href="https://msdn.microsoft.com/dd44f256-9423-4f29-aba3-6b0554349864">DOT11_RADIO_STATE</a> value that indicates the software radio state.


### -field dot11HardwareRadioState

A <a href="https://msdn.microsoft.com/dd44f256-9423-4f29-aba3-6b0554349864">DOT11_RADIO_STATE</a> value that indicates the hardware radio state.


## -remarks



The <b>WLAN_PHY_RADIO_STATE</b> structure is used with the <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> function when the <i>OpCode</i> parameter is set to <b>wlan_intf_opcode_radio_state</b>. 

The <b>WLAN_PHY_RADIO_STATE</b> structure is also used for  notification by the media specific module (MSM) when the radio state changes. An application registers to receive MSM notifications by calling the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function with the <i>dwNotifSource</i> parameter set to a value that includes <b>WLAN_NOTIFICATION_SOURCE_MSM</b>. For more information on these notifications, see the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure and the <a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a> enumeration reference.

The radio state of a PHY is off if either <b>dot11SoftwareRadioState</b> or <b>dot11HardwareRadioState</b> member of the <b>WLAN_PHY_RADIO_STATE</b> structure is <b>dot11_radio_state_off</b>.

The hardware radio state cannot be changed by calling the <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> function.  The <b>dot11HardwareRadioState</b> member of the <b>WLAN_PHY_RADIO_STATE</b> structure is ignored when  the <b>WlanSetInterface</b> function is called with the <i>OpCode</i> parameter set to <b>wlan_intf_opcode_radio_state</b> and the <i>pData</i> parameter points to a <b>WLAN_PHY_RADIO_STATE</b> structure. 

The software radio state can be changed by calling the <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> function.   

Changing the software radio state of a physical network interface could cause related changes in the state of the wireless Hosted Network or virtual wireless adapter radio states. The PHYs of every virtual wireless adapter are linked. For more information, see the <a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>.

The radio state of a PHY is off if either the software radio state (<b>dot11SoftwareRadioState</b> member) or the hardware radio state (<b>dot11HardwareRadioState</b> member) is off.   




## -see-also




<a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>



<a href="https://msdn.microsoft.com/dd44f256-9423-4f29-aba3-6b0554349864">DOT11_RADIO_STATE</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a>



<a href="https://msdn.microsoft.com/61551b46-785e-4353-910c-8ce23172b176">WLAN_RADIO_STATE</a>



<a href="https://msdn.microsoft.com/09f8273a-5259-44fa-b55e-af3282735c0b">WlanGetInterfaceCapability</a>



<a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a>
 

 

