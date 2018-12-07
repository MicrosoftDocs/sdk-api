---
UID: NS:wlanapi._WLAN_RATE_SET
title: "_WLAN_RATE_SET"
author: windows-sdk-content
description: The set of supported data rates.
old-location: nwifi\wlan_rate_set.htm
tech.root: NativeWiFi
ms.assetid: e07a9249-9571-4747-b913-05d319202f8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_RATE_SET, PWLAN_RATE_SET, PWLAN_RATE_SET structure pointer [NativeWIFI], WLAN_RATE_SET, WLAN_RATE_SET structure [NativeWIFI], _WLAN_RATE_SET, nwifi.wlan_rate_set, wlanapi/PWLAN_RATE_SET, wlanapi/WLAN_RATE_SET"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WLAN_RATE_SET
product: Windows
targetos: Windows
req.typenames: WLAN_RATE_SET, *PWLAN_RATE_SET
req.redist: 
---

# _WLAN_RATE_SET structure


## -description


The set of supported data rates.


## -struct-fields




### -field uRateSetLength

The length, in bytes, of <b>usRateSet</b>.


### -field usRateSet

An array of supported data transfer rates. DOT11_RATE_SET_MAX_LENGTH  is defined in windot11.h to have a value of 126.

Each supported data transfer rate is stored as a USHORT. The first bit of the USHORT specifies whether the rate is a basic rate. A <i>basic rate</i> is the data transfer rate that all stations in a basic service set (BSS) can use to receive frames from the wireless medium. If the rate is a basic rate, the first bit of the USHORT is set to 1.

To calculate the data transfer rate in Mbps for an arbitrary array entry rateSet[i], use the following equation:

<code>rate_in_mbps = (rateSet[i] &amp; 0x7FFF) * 0.5</code>


## -see-also




<a href="https://msdn.microsoft.com/25a76128-13d9-47dd-9c73-1fbf06a908be">WLAN_BSS_ENTRY</a>
 

 

