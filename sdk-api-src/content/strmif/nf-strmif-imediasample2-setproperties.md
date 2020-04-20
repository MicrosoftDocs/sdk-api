---
UID: NF:strmif.IMediaSample2.SetProperties
title: IMediaSample2::SetProperties (strmif.h)
description: The SetProperties method sets the properties of a media sample.helpviewer_keywords: ["IMediaSample2 interface [DirectShow]","SetProperties method","IMediaSample2.SetProperties","IMediaSample2::SetProperties","IMediaSample2SetProperties","SetProperties","SetProperties method [DirectShow]","SetProperties method [DirectShow]","IMediaSample2 interface","dshow.imediasample2_setproperties","strmif/IMediaSample2::SetProperties"]
old-location: dshow\imediasample2_setproperties.htm
tech.root: DirectShow
ms.assetid: f024fe3a-802d-4dc1-9f4d-ebeeed0b067a
ms.date: 12/05/2018
ms.keywords: IMediaSample2 interface [DirectShow],SetProperties method, IMediaSample2.SetProperties, IMediaSample2::SetProperties, IMediaSample2SetProperties, SetProperties, SetProperties method [DirectShow], SetProperties method [DirectShow],IMediaSample2 interface, dshow.imediasample2_setproperties, strmif/IMediaSample2::SetProperties
f1_keywords:
- strmif/IMediaSample2.SetProperties
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
- IMediaSample2.SetProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSample2::SetProperties


## -description



The <b>SetProperties</b> method sets the properties of a media sample.




## -parameters




### -param cbProperties [in]

Length of property data to set, in bytes.


### -param pbProperties [in]

Pointer to a buffer of size <i>cbProperties</i>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



The data contained in [AM_SAMPLE2_PROPERTIES](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_sample2_properties) structure. You can specify a subset of the sample properties by setting <i>cbProperties</i> to a value less than the size of the <b>AM_SAMPLE2_PROPERTIES</b> structure.

The standard implementation of this method does not support updating [AM_SAMPLE2_PROPERTIES](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_sample2_properties) structure. If these members are not equal to zero, the method returns <b>E_INVALIDARG</b>. To modify the data contained in the sample's memory buffer, call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-getpointer">IMediaSample::GetPointer</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediasample2">IMediaSample2 Interface</a>
 

 

