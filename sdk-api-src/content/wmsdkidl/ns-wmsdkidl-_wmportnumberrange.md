---
UID: NS:wmsdkidl._WMPortNumberRange
title: "_WMPortNumberRange"
author: windows-sdk-content
description: The WM_PORT_NUMBER_RANGE structure describes the range of port numbers used by the IWMReaderNetworkConfig interface.
old-location: wmformat\wm_port_number_range.htm
tech.root: wmformat
ms.assetid: 122db3fa-36bb-4d0c-9d05-0b7ae37f9187
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WM_PORT_NUMBER_RANGE, WM_PORT_NUMBER_RANGE structure [windows Media Format], _WMPortNumberRange, structure [windows Media Format], wmformat.wm_port_number_range, wmsdkidl/WM_PORT_NUMBER_RANGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wmsdkidl.h
api_name:
 - WM_PORT_NUMBER_RANGE
product: Windows
targetos: Windows
req.typenames: WM_PORT_NUMBER_RANGE
req.redist: 
---

# _WMPortNumberRange structure


## -description



The <b>WM_PORT_NUMBER_RANGE</b> structure describes the range of port numbers used by the <b>IWMReaderNetworkConfig</b> interface.




## -struct-fields




### -field wPortBegin

<b>WORD</b> containing the lowest port number.


### -field wPortEnd

<b>WORD</b> containing the highest port number.


## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/a1792fd0-e9c3-4e28-9928-a615e1c9aec8">IWMReaderNetworkConfig::GetUDPPortRanges</a>



<a href="https://msdn.microsoft.com/9a61943a-8ff9-4504-b76f-25e3c5c8d4a4">IWMReaderNetworkConfig::SetUDPPortRanges</a>



<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

