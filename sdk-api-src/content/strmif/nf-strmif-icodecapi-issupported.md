---
UID: NF:strmif.ICodecAPI.IsSupported
title: ICodecAPI::IsSupported (strmif.h)
description: The IsSupported method queries whether a codec supports a given property.
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","IsSupported method","ICodecAPI.IsSupported","ICodecAPI::IsSupported","ICodecAPIIsSupported","IsSupported","IsSupported method [DirectShow]","IsSupported method [DirectShow]","ICodecAPI interface","dshow.icodecapi_issupported","strmif/ICodecAPI::IsSupported"]
old-location: dshow\icodecapi_issupported.htm
tech.root: DirectShow
ms.assetid: 6f556532-1a49-45c1-b446-89c05e8a8237
ms.date: 12/05/2018
ms.keywords: ICodecAPI interface [DirectShow],IsSupported method, ICodecAPI.IsSupported, ICodecAPI::IsSupported, ICodecAPIIsSupported, IsSupported, IsSupported method [DirectShow], IsSupported method [DirectShow],ICodecAPI interface, dshow.icodecapi_issupported, strmif/ICodecAPI::IsSupported
f1_keywords:
- strmif/ICodecAPI.IsSupported
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- ICodecAPI.IsSupported
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICodecAPI::IsSupported


## -description



The <b>IsSupported</b> method queries whether a codec supports a given property.




## -parameters




### -param Api [in]

Pointer to a GUID that specifies the property to query. For a list of standard codec properties, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.
          


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The codec does not support the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The codec supports the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The codec does not support the property.

</td>
</tr>
</table>
 




## -remarks



Any errors besides those in the previous table indicate an inability to process the call.

<div class="alert"><b>Note</b>  If the codec does not support the property, the method can return either <b>S_FALSE</b> or <b>E_NOTIMPL</b>. The value <b>E_NOTIMPL</b> is preferred, but earlier documentation listed only <b>S_FALSE</b>, so some codecs might return that value. Applications should explicitly test for the value <b>S_OK</b>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
 

 

