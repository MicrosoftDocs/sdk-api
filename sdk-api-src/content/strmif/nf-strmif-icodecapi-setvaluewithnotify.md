---
UID: NF:strmif.ICodecAPI.SetValueWithNotify
title: ICodecAPI::SetValueWithNotify (strmif.h)
description: The SetValueWithNotify method sets a property on a codec and returns a list of other properties that changed as a result.helpviewer_keywords: ["ICodecAPI interface [DirectShow]","SetValueWithNotify method","ICodecAPI.SetValueWithNotify","ICodecAPI::SetValueWithNotify","ICodecAPISetValueWithNotify","SetValueWithNotify","SetValueWithNotify method [DirectShow]","SetValueWithNotify method [DirectShow]","ICodecAPI interface","dshow.icodecapi_setvaluewithnotify","strmif/ICodecAPI::SetValueWithNotify"]
old-location: dshow\icodecapi_setvaluewithnotify.htm
tech.root: DirectShow
ms.assetid: b2899e30-4dfb-47e7-88dd-adba49368a4f
ms.date: 12/05/2018
ms.keywords: ICodecAPI interface [DirectShow],SetValueWithNotify method, ICodecAPI.SetValueWithNotify, ICodecAPI::SetValueWithNotify, ICodecAPISetValueWithNotify, SetValueWithNotify, SetValueWithNotify method [DirectShow], SetValueWithNotify method [DirectShow],ICodecAPI interface, dshow.icodecapi_setvaluewithnotify, strmif/ICodecAPI::SetValueWithNotify
f1_keywords:
- strmif/ICodecAPI.SetValueWithNotify
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
- ICodecAPI.SetValueWithNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICodecAPI::SetValueWithNotify


## -description



The <b>SetValueWithNotify</b> method sets a property on a codec and returns a list of other properties that changed as a result.




## -parameters




### -param Api [in]

Pointer to a GUID that specifies the property to set.
          For a list of standard codec properties, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.


### -param Value [in]

Pointer to a <b>VARIANT</b>  that contains the new value for the property.
          


### -param ChangedParam [out]

Receives a pointer to an array of GUIDs. The array contains the GUIDs of any properties that changed as a result of this method call. The caller must free the array by calling <b>CoTaskMemFree</b>.
          


### -param ChangedParamCount [out]

Receives the number of elements in the <i>ChangedParam</i> array.
          


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



Codecs that implement <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> are  not required to support this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-getvalue">ICodecAPI::GetValue</a>
 

 

