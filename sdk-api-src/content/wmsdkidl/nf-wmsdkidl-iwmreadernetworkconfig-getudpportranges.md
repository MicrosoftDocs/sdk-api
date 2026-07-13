---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetUDPPortRanges
title: IWMReaderNetworkConfig::GetUDPPortRanges (wmsdkidl.h)
description: The GetUDPPortRanges method retrieves the UDP port number ranges used for receiving data.
helpviewer_keywords: ["GetUDPPortRanges","GetUDPPortRanges method [windows Media Format]","GetUDPPortRanges method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetUDPPortRanges method","IWMReaderNetworkConfig.GetUDPPortRanges","IWMReaderNetworkConfig::GetUDPPortRanges","IWMReaderNetworkConfigGetUDPPortRanges","wmformat.iwmreadernetworkconfig_getudpportranges","wmsdkidl/IWMReaderNetworkConfig::GetUDPPortRanges"]
old-location: wmformat\iwmreadernetworkconfig_getudpportranges.htm
tech.root: wmformat
ms.assetid: a1792fd0-e9c3-4e28-9928-a615e1c9aec8
ms.date: 4/26/2023
ms.keywords: GetUDPPortRanges, GetUDPPortRanges method [windows Media Format], GetUDPPortRanges method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetUDPPortRanges method, IWMReaderNetworkConfig.GetUDPPortRanges, IWMReaderNetworkConfig::GetUDPPortRanges, IWMReaderNetworkConfigGetUDPPortRanges, wmformat.iwmreadernetworkconfig_getudpportranges, wmsdkidl/IWMReaderNetworkConfig::GetUDPPortRanges
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
 - IWMReaderNetworkConfig::GetUDPPortRanges
 - wmsdkidl/IWMReaderNetworkConfig::GetUDPPortRanges
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
 - IWMReaderNetworkConfig.GetUDPPortRanges
---

# IWMReaderNetworkConfig::GetUDPPortRanges


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetUDPPortRanges</b> method retrieves the UDP port number ranges used for receiving data.

## -parameters

### -param pRangeArray [out]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range">WM_PORT_NUMBER_RANGE</a> structures allocated by the caller. Pass <b>NULL</b> to get the size of the array.

### -param pcRanges [in, out]

On input, pointer to a <b>DWORD</b> containing the length of the array passed in <i>pRangeArray</i>. On output, pointer to the required array size.

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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcRanges</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You should make two calls to this method. On the first call, pass <b>NULL</b> for <i>pRangeArray</i>. On return, the value pointed to by <i>pcRanges</i> is set to the size of the array that you should allocate. Then you can allocate the required amount of memory for the array and pass a pointer to it as <i>pRangeArray</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setudpportranges">IWMReaderNetworkConfig::SetUDPPortRanges</a>