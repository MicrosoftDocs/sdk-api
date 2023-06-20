---
UID: NF:wmsdkidl.IWMReaderAdvanced4.IsUsingFastCache
title: IWMReaderAdvanced4::IsUsingFastCache (wmsdkidl.h)
description: The IsUsingFastCache method queries whether the reader is using Fast Cache streaming.
helpviewer_keywords: ["IWMReaderAdvanced4 interface [windows Media Format]","IsUsingFastCache method","IWMReaderAdvanced4.IsUsingFastCache","IWMReaderAdvanced4::IsUsingFastCache","IWMReaderAdvanced4IsUsingFastCache","IsUsingFastCache","IsUsingFastCache method [windows Media Format]","IsUsingFastCache method [windows Media Format]","IWMReaderAdvanced4 interface","wmformat.iwmreaderadvanced4_isusingfastcache","wmsdkidl/IWMReaderAdvanced4::IsUsingFastCache"]
old-location: wmformat\iwmreaderadvanced4_isusingfastcache.htm
tech.root: wmformat
ms.assetid: 29d8d12c-db4c-4c2c-8747-30c8a5577f43
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced4 interface [windows Media Format],IsUsingFastCache method, IWMReaderAdvanced4.IsUsingFastCache, IWMReaderAdvanced4::IsUsingFastCache, IWMReaderAdvanced4IsUsingFastCache, IsUsingFastCache, IsUsingFastCache method [windows Media Format], IsUsingFastCache method [windows Media Format],IWMReaderAdvanced4 interface, wmformat.iwmreaderadvanced4_isusingfastcache, wmsdkidl/IWMReaderAdvanced4::IsUsingFastCache
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
 - IWMReaderAdvanced4::IsUsingFastCache
 - wmsdkidl/IWMReaderAdvanced4::IsUsingFastCache
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
 - IWMReaderAdvanced4.IsUsingFastCache
---

# IWMReaderAdvanced4::IsUsingFastCache


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IsUsingFastCache</b> method queries whether the reader is using Fast Cache streaming.

## -parameters

### -param pfUsingFastCache [out]

Pointer to a variable that receives a Boolean value. The value is True if the reader is currently using Fast Cache streaming, or False otherwise.

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

## -see-also

<a href="/windows/desktop/wmformat/enabling-fast-cache-streaming-from-the-client">Enabling Fast Cache Streaming from the Client</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>