---
UID: NF:wmsdkidl.IWMReaderAdvanced4.IsUsingFastCache
title: IWMReaderAdvanced4::IsUsingFastCache (wmsdkidl.h)
description: The IsUsingFastCache method queries whether the reader is using Fast Cache streaming.
helpviewer_keywords: ["IWMReaderAdvanced4 interface [windows Media Format]","IsUsingFastCache method","IWMReaderAdvanced4.IsUsingFastCache","IWMReaderAdvanced4::IsUsingFastCache","IWMReaderAdvanced4IsUsingFastCache","IsUsingFastCache","IsUsingFastCache method [windows Media Format]","IsUsingFastCache method [windows Media Format]","IWMReaderAdvanced4 interface","wmformat.iwmreaderadvanced4_isusingfastcache","wmsdkidl/IWMReaderAdvanced4::IsUsingFastCache"]
old-location: wmformat\iwmreaderadvanced4_isusingfastcache.htm
tech.root: wmformat
ms.assetid: 29d8d12c-db4c-4c2c-8747-30c8a5577f43
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced4 interface [windows Media Format],IsUsingFastCache method, IWMReaderAdvanced4.IsUsingFastCache, IWMReaderAdvanced4::IsUsingFastCache, IWMReaderAdvanced4IsUsingFastCache, IsUsingFastCache, IsUsingFastCache method [windows Media Format], IsUsingFastCache method [windows Media Format],IWMReaderAdvanced4 interface, wmformat.iwmreaderadvanced4_isusingfastcache, wmsdkidl/IWMReaderAdvanced4::IsUsingFastCache
f1_keywords:
- wmsdkidl/IWMReaderAdvanced4.IsUsingFastCache
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced4::IsUsingFastCache


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/wmformat/enabling-fast-cache-streaming-from-the-client">Enabling Fast Cache Streaming from the Client</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>
 

 

