---
UID: NS:wlanapi._WLAN_PHY_RADIO_STATE
title: WLAN_PHY_RADIO_STATE (wlanapi.h)
description: Specifies the radio state.
helpviewer_keywords: ["*PWLAN_PHY_RADIO_STATE","PWLAN_PHY_RADIO_STATE","PWLAN_PHY_RADIO_STATE structure pointer [NativeWIFI]","WLAN_PHY_RADIO_STATE","WLAN_PHY_RADIO_STATE structure [NativeWIFI]","nwifi.wlan_phy_radio_state","wlanapi/PWLAN_PHY_RADIO_STATE","wlanapi/WLAN_PHY_RADIO_STATE"]
old-location: nwifi\wlan_phy_radio_state.htm
tech.root: nwifi
ms.assetid: 20da1494-4264-4d0d-b789-25e2be6a8dd4
ms.date: 12/05/2018
ms.keywords: '*PWLAN_PHY_RADIO_STATE, PWLAN_PHY_RADIO_STATE, PWLAN_PHY_RADIO_STATE structure pointer [NativeWIFI], WLAN_PHY_RADIO_STATE, WLAN_PHY_RADIO_STATE structure [NativeWIFI], nwifi.wlan_phy_radio_state, wlanapi/PWLAN_PHY_RADIO_STATE, wlanapi/WLAN_PHY_RADIO_STATE'
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
targetos: Windows
req.typenames: WLAN_PHY_RADIO_STATE, *PWLAN_PHY_RADIO_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_PHY_RADIO_STATE
 - wlanapi/_WLAN_PHY_RADIO_STATE
 - PWLAN_PHY_RADIO_STATE
 - wlanapi/PWLAN_PHY_RADIO_STATE
 - WLAN_PHY_RADIO_STATE
 - wlanapi/WLAN_PHY_RADIO_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_PHY_RADIO_STATE
---

# WLAN_PHY_RADIO_STATE structure


## -description

The <b>WLAN_PHY_RADIO_STATE</b> structure specifies the radio state on a specific physical layer (PHY) type.

## -struct-fields

### -field dwPhyIndex

The index of the PHY type on which the radio state is being set or queried. The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability">WlanGetInterfaceCapability</a> function returns a list of valid PHY types.

### -field dot11SoftwareRadioState

A <a href="/windows/win32/api/wlanapi/ne-wlanapi-dot11_radio_state-r1">DOT11_RADIO_STATE</a> value that indicates the software radio state.

### -field dot11HardwareRadioState

A <a href="/windows/win32/api/wlanapi/ne-wlanapi-dot11_radio_state-r1">DOT11_RADIO_STATE</a> value that indicates the hardware radio state.

## -remarks

The <b>WLAN_PHY_RADIO_STATE</b> structure is used with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> function when the <i>OpCode</i> parameter is set to <b>wlan_intf_opcode_radio_state</b>. 

The <b>WLAN_PHY_RADIO_STATE</b> structure is also used for  notification by the media specific module (MSM) when the radio state changes. An application registers to receive MSM notifications by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function with the <i>dwNotifSource</i> parameter set to a value that includes <b>WLAN_NOTIFICATION_SOURCE_MSM</b>. For more information on these notifications, see the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure and the <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_notification_msm-r1">WLAN_NOTIFICATION_MSM</a> enumeration reference.

The radio state of a PHY is off if either <b>dot11SoftwareRadioState</b> or <b>dot11HardwareRadioState</b> member of the <b>WLAN_PHY_RADIO_STATE</b> structure is <b>dot11_radio_state_off</b>.

The hardware radio state cannot be changed by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> function.  The <b>dot11HardwareRadioState</b> member of the <b>WLAN_PHY_RADIO_STATE</b> structure is ignored when  the <b>WlanSetInterface</b> function is called with the <i>OpCode</i> parameter set to <b>wlan_intf_opcode_radio_state</b> and the <i>pData</i> parameter points to a <b>WLAN_PHY_RADIO_STATE</b> structure. 

The software radio state can be changed by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> function.   

Changing the software radio state of a physical network interface could cause related changes in the state of the wireless Hosted Network or virtual wireless adapter radio states. The PHYs of every virtual wireless adapter are linked. For more information, see the <a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>.

The radio state of a PHY is off if either the software radio state (<b>dot11SoftwareRadioState</b> member) or the hardware radio state (<b>dot11HardwareRadioState</b> member) is off.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-dot11_radio_state-r1">DOT11_RADIO_STATE</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_notification_msm-r1">WLAN_NOTIFICATION_MSM</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_radio_state">WLAN_RADIO_STATE</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability">WlanGetInterfaceCapability</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a>