---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetEnableFastCache
title: IWMReaderNetworkConfig2::GetEnableFastCache (wmsdkidl.h)
description: The GetEnableFastCache method queries whether Fast Cache streaming is enabled. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.
helpviewer_keywords: ["GetEnableFastCache","GetEnableFastCache method [windows Media Format]","GetEnableFastCache method [windows Media Format]","IWMReaderNetworkConfig2 interface","IWMReaderNetworkConfig2 interface [windows Media Format]","GetEnableFastCache method","IWMReaderNetworkConfig2.GetEnableFastCache","IWMReaderNetworkConfig2::GetEnableFastCache","IWMReaderNetworkConfig2GetEnableFastCache","wmformat.iwmreadernetworkconfig2_getenablefastcache","wmsdkidl/IWMReaderNetworkConfig2::GetEnableFastCache"]
old-location: wmformat\iwmreadernetworkconfig2_getenablefastcache.htm
tech.root: wmformat
ms.assetid: 50f904a3-5a2d-4c0f-92fe-76a1ff195c91
ms.date: 4/26/2023
ms.keywords: GetEnableFastCache, GetEnableFastCache method [windows Media Format], GetEnableFastCache method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetEnableFastCache method, IWMReaderNetworkConfig2.GetEnableFastCache, IWMReaderNetworkConfig2::GetEnableFastCache, IWMReaderNetworkConfig2GetEnableFastCache, wmformat.iwmreadernetworkconfig2_getenablefastcache, wmsdkidl/IWMReaderNetworkConfig2::GetEnableFastCache
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMReaderNetworkConfig2::GetEnableFastCache
 - wmsdkidl/IWMReaderNetworkConfig2::GetEnableFastCache
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
 - IWMReaderNetworkConfig2.GetEnableFastCache
---

# IWMReaderNetworkConfig2::GetEnableFastCache


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetEnableFastCache</b> method queries whether Fast Cache streaming is enabled. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.

## -parameters

### -param pfEnableFastCache [out]

Pointer to a variable that receives a Boolean value. The value is True if Fast Cache streaming is enabled, or False otherwise.

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
NULL pointer argument.

</td>
</tr>
</table>

## -remarks

This feature requires content caching to be enabled as well. Fast Cache applies only to content being streamed from a server running Windows Media Services.

## -see-also

<a href="/windows/desktop/wmformat/enabling-fast-cache-streaming-from-the-client">Enabling Fast Cache Streaming from the Client</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache">IWMReaderNetworkConfig2::SetEnableFastCache</a>