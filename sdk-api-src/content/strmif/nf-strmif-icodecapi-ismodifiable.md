---
UID: NF:strmif.ICodecAPI.IsModifiable
title: ICodecAPI::IsModifiable (strmif.h)
description: The IsModifiable method queries whether a codec property can be changed, given the codec's current configuration.helpviewer_keywords: ["ICodecAPI interface [DirectShow]","IsModifiable method","ICodecAPI.IsModifiable","ICodecAPI::IsModifiable","ICodecAPIIsModifiable","IsModifiable","IsModifiable method [DirectShow]","IsModifiable method [DirectShow]","ICodecAPI interface","dshow.icodecapi_ismodifiable","strmif/ICodecAPI::IsModifiable"]
old-location: dshow\icodecapi_ismodifiable.htm
tech.root: DirectShow
ms.assetid: 5f7c7f72-02f2-4840-aaa2-9d26fe564577
ms.date: 12/05/2018
ms.keywords: ICodecAPI interface [DirectShow],IsModifiable method, ICodecAPI.IsModifiable, ICodecAPI::IsModifiable, ICodecAPIIsModifiable, IsModifiable, IsModifiable method [DirectShow], IsModifiable method [DirectShow],ICodecAPI interface, dshow.icodecapi_ismodifiable, strmif/ICodecAPI::IsModifiable
f1_keywords:
- strmif/ICodecAPI.IsModifiable
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
- ICodecAPI.IsModifiable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICodecAPI::IsModifiable


## -description


The <b>IsModifiable</b> method queries whether a codec property can be changed, given the codec's current configuration.
      


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.


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
The value of this property cannot be changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The value of this property can be changed.

</td>
</tr>
</table>
 




## -remarks



Any errors besides those in the previous table indicate an inability to process the call.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
 

 

