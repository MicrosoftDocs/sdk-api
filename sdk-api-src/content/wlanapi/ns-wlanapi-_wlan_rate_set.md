---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

