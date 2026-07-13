---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetEnableFastCache
title: IWMReaderNetworkConfig2::SetEnableFastCache (wmsdkidl.h)
description: The SetEnableFastCache method enables or disables Fast Cache streaming. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.
helpviewer_keywords: ["IWMReaderNetworkConfig2 interface [windows Media Format]","SetEnableFastCache method","IWMReaderNetworkConfig2.SetEnableFastCache","IWMReaderNetworkConfig2::SetEnableFastCache","IWMReaderNetworkConfig2SetEnableFastCache","SetEnableFastCache","SetEnableFastCache method [windows Media Format]","SetEnableFastCache method [windows Media Format]","IWMReaderNetworkConfig2 interface","wmformat.iwmreadernetworkconfig2_setenablefastcache","wmsdkidl/IWMReaderNetworkConfig2::SetEnableFastCache"]
old-location: wmformat\iwmreadernetworkconfig2_setenablefastcache.htm
tech.root: wmformat
ms.assetid: 28a01985-a133-4203-8385-d4497c29bf9c
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetEnableFastCache method, IWMReaderNetworkConfig2.SetEnableFastCache, IWMReaderNetworkConfig2::SetEnableFastCache, IWMReaderNetworkConfig2SetEnableFastCache, SetEnableFastCache, SetEnableFastCache method [windows Media Format], SetEnableFastCache method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setenablefastcache, wmsdkidl/IWMReaderNetworkConfig2::SetEnableFastCache
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
 - IWMReaderNetworkConfig2::SetEnableFastCache
 - wmsdkidl/IWMReaderNetworkConfig2::SetEnableFastCache
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
 - IWMReaderNetworkConfig2.SetEnableFastCache
---

# IWMReaderNetworkConfig2::SetEnableFastCache


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetEnableFastCache</b> method enables or disables Fast Cache streaming. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.

## -parameters

### -param fEnableFastCache [in]

Specifies whether to enable or disable Fast Cache streaming. The value True enables Fast Cache, and the value False disables it.

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
</table>

## -remarks

This method enables the reader to use Fast Cache streaming if the server also supports it. This feature is supported only when streaming content from a server running Windows Media Services. For more information, see <a href="/windows/desktop/wmformat/enabling-fast-cache-streaming-from-the-client">Enabling Fast Cache Streaming from the Client</a>.

Regardless of the status of Fast Cache set by this method, a user can enable this feature by adding "?WMCache=1" to the end of the URL. However, Fast Cache cannot be activated at all unless caching is enabled with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching">IWMReaderNetworkconfig2::SetEnableContentCaching</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getenablefastcache">IWMReaderNetworkConfig2::GetEnableFastCache</a>