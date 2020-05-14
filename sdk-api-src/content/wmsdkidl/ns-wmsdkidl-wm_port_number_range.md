---
UID: NS:wmsdkidl._WMPortNumberRange
title: WM_PORT_NUMBER_RANGE (wmsdkidl.h)
description: The WM_PORT_NUMBER_RANGE structure describes the range of port numbers used by the IWMReaderNetworkConfig interface.helpviewer_keywords: ["WM_PORT_NUMBER_RANGE","WM_PORT_NUMBER_RANGE structure [windows Media Format]","structure [windows Media Format]","wmformat.wm_port_number_range","wmsdkidl/WM_PORT_NUMBER_RANGE"]
old-location: wmformat\wm_port_number_range.htm
tech.root: wmformat
ms.assetid: 122db3fa-36bb-4d0c-9d05-0b7ae37f9187
ms.date: 12/05/2018
ms.keywords: WM_PORT_NUMBER_RANGE, WM_PORT_NUMBER_RANGE structure [windows Media Format], structure [windows Media Format], wmformat.wm_port_number_range, wmsdkidl/WM_PORT_NUMBER_RANGE
f1_keywords:
- wmsdkidl/WM_PORT_NUMBER_RANGE
dev_langs:
- c++
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
targetos: Windows
req.typenames: WM_PORT_NUMBER_RANGE
req.redist: 
ms.custom: 19H1
---

# WM_PORT_NUMBER_RANGE structure


## -description



The <b>WM_PORT_NUMBER_RANGE</b> structure describes the range of port numbers used by the <b>IWMReaderNetworkConfig</b> interface.




## -struct-fields




### -field wPortBegin

<b>WORD</b> containing the lowest port number.


### -field wPortEnd

<b>WORD</b> containing the highest port number.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getudpportranges">IWMReaderNetworkConfig::GetUDPPortRanges</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setudpportranges">IWMReaderNetworkConfig::SetUDPPortRanges</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/structures">Structures</a>
 

 

