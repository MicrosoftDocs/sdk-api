---
UID: NF:mediaobj.IMediaObject.GetInputType
title: IMediaObject::GetInputType (mediaobj.h)
description: The GetInputType method retrieves a preferred media type for a specified input stream.
helpviewer_keywords: ["GetInputType","GetInputType method [DirectShow]","GetInputType method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetInputType method","IMediaObject.GetInputType","IMediaObject::GetInputType","IMediaObjectGetInputType","dshow.imediaobject_getinputtype","mediaobj/IMediaObject::GetInputType"]
old-location: dshow\imediaobject_getinputtype.htm
tech.root: dshow
ms.assetid: 22693a22-97be-487d-ad17-31a2d8ee874c
ms.date: 12/05/2018
ms.keywords: GetInputType, GetInputType method [DirectShow], GetInputType method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputType method, IMediaObject.GetInputType, IMediaObject::GetInputType, IMediaObjectGetInputType, dshow.imediaobject_getinputtype, mediaobj/IMediaObject::GetInputType
f1_keywords:
- mediaobj/IMediaObject.GetInputType
dev_langs:
- c++
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dmoguids.lib
- Dmoguids.dll
api_name:
- IMediaObject.GetInputType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaObject::GetInputType


## -description



The <code>GetInputType</code> method retrieves a preferred media type for a specified input stream.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param dwTypeIndex

Zero-based index on the set of acceptable media types.


### -param pmt [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure allocated by the caller, or <b>NULL</b>. If this parameter is non-<b>NULL</b>, the method fills the structure with the media type. You can use the value <b>NULL</b> to test whether the type index is in range, by checking the return code.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
Type index is out of range.

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
</table>
 




## -remarks



Call this method to enumerate an input stream's preferred media types. The DMO assigns each media type an index value in order of preference. The most preferred type has an index of zero. To enumerate all the types, make successive calls while incrementing the type index until the method returns DMO_E_NO_MORE_ITEMS. The DMO is not guaranteed to enumerate every media type that it supports.

The format block in the returned type might be <b>NULL</b>. If so, the format type is GUID_NULL. Check the format type before dereferencing the format block.

If the method succeeds, call <a href="https://docs.microsoft.com/windows/desktop/api/dmort/nf-dmort-mofreemediatype">MoFreeMediaType</a> to free the format block. (This function is also safe to call when the format block is <b>NULL</b>.)

To set the media type, call the <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype">IMediaObject::SetInputType</a> method. Setting the media type on one stream can change another stream's preferred types. In fact, a stream might not have a preferred type until the type is set on another stream. For example, a decoder might not have a preferred output type until the input type is set. However, the DMO is not required to update its preferred types dynamically in this fashion. Thus, the types returned by this method are not guaranteed to be valid; they might fail when used in the <b>SetInputType</b> method.

To test whether a particular media type is acceptable, call <b>SetInputType</b> with the DMO_SET_TYPEF_TEST_ONLY flag.

To test whether the <i>dwTypeIndex</i> parameter is in range, set <i>pmt</i> to <b>NULL</b>. The method returns S_OK if the index is in range, or DMO_E_NO_MORE_ITEMS if the index is out of range.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>
 

 

