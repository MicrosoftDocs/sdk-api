---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetUDPPortRanges
title: IWMReaderNetworkConfig::SetUDPPortRanges (wmsdkidl.h)
description: The SetUDPPortRanges method specifies the UDP port number ranges that are used for receiving data.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetUDPPortRanges method","IWMReaderNetworkConfig.SetUDPPortRanges","IWMReaderNetworkConfig::SetUDPPortRanges","IWMReaderNetworkConfigSetUDPPortRanges","SetUDPPortRanges","SetUDPPortRanges method [windows Media Format]","SetUDPPortRanges method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setudpportranges","wmsdkidl/IWMReaderNetworkConfig::SetUDPPortRanges"]
old-location: wmformat\iwmreadernetworkconfig_setudpportranges.htm
tech.root: wmformat
ms.assetid: 9a61943a-8ff9-4504-b76f-25e3c5c8d4a4
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetUDPPortRanges method, IWMReaderNetworkConfig.SetUDPPortRanges, IWMReaderNetworkConfig::SetUDPPortRanges, IWMReaderNetworkConfigSetUDPPortRanges, SetUDPPortRanges, SetUDPPortRanges method [windows Media Format], SetUDPPortRanges method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setudpportranges, wmsdkidl/IWMReaderNetworkConfig::SetUDPPortRanges
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderNetworkConfig::SetUDPPortRanges
 - wmsdkidl/IWMReaderNetworkConfig::SetUDPPortRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderNetworkConfig.SetUDPPortRanges
---

# IWMReaderNetworkConfig::SetUDPPortRanges


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetUDPPortRanges</b> method specifies the UDP port number ranges that are used for receiving data.

## -parameters

### -param pRangeArray [in]

Pointer to an array of <b>WM_PORT_NUMBER_RANGE</b> structures.

### -param cRanges [in]

A value indicating the length of the array passed in <i>pRangeArray</i>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL or invalid argument passed in.

</td>
</tr>
</table>

## -remarks

If no ranges are specified by the application, port numbers are selected by the reader.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getudpportranges">IWMReaderNetworkConfig::GetUDPPortRanges</a>



<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range">WM_PORT_NUMBER_RANGE</a>