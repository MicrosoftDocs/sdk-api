---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetEnableMulticast
title: IWMReaderNetworkConfig::GetEnableMulticast (wmsdkidl.h)
description: The GetEnableMulticast method ascertains whether multicast is enabled.
helpviewer_keywords: ["GetEnableMulticast","GetEnableMulticast method [windows Media Format]","GetEnableMulticast method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetEnableMulticast method","IWMReaderNetworkConfig.GetEnableMulticast","IWMReaderNetworkConfig::GetEnableMulticast","IWMReaderNetworkConfigGetEnableMulticast","wmformat.iwmreadernetworkconfig_getenablemulticast","wmsdkidl/IWMReaderNetworkConfig::GetEnableMulticast"]
old-location: wmformat\iwmreadernetworkconfig_getenablemulticast.htm
tech.root: wmformat
ms.assetid: 2fc51a74-18b6-4ddd-9089-9a8bdfce70ea
ms.date: 4/26/2023
ms.keywords: GetEnableMulticast, GetEnableMulticast method [windows Media Format], GetEnableMulticast method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetEnableMulticast method, IWMReaderNetworkConfig.GetEnableMulticast, IWMReaderNetworkConfig::GetEnableMulticast, IWMReaderNetworkConfigGetEnableMulticast, wmformat.iwmreadernetworkconfig_getenablemulticast, wmsdkidl/IWMReaderNetworkConfig::GetEnableMulticast
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
 - IWMReaderNetworkConfig::GetEnableMulticast
 - wmsdkidl/IWMReaderNetworkConfig::GetEnableMulticast
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
 - IWMReaderNetworkConfig.GetEnableMulticast
---

# IWMReaderNetworkConfig::GetEnableMulticast


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetEnableMulticast</b> method ascertains whether multicast is enabled.

## -parameters

### -param pfEnableMulticast [out]

Pointer to a Boolean value that is set to True if multicast has been enabled.

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

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenablemulticast">IWMReaderNetworkConfig::SetEnableMulticast</a>