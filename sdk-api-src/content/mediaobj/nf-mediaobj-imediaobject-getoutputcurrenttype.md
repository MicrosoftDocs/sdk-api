---
UID: NF:mediaobj.IMediaObject.GetOutputCurrentType
title: IMediaObject::GetOutputCurrentType (mediaobj.h)
description: The GetOutputCurrentType method retrieves the media type that was set for an output stream, if any.
helpviewer_keywords: ["GetOutputCurrentType","GetOutputCurrentType method [DirectShow]","GetOutputCurrentType method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetOutputCurrentType method","IMediaObject.GetOutputCurrentType","IMediaObject::GetOutputCurrentType","IMediaObjectGetOutputCurrentType","dshow.imediaobject_getoutputcurrenttype","mediaobj/IMediaObject::GetOutputCurrentType"]
old-location: dshow\imediaobject_getoutputcurrenttype.htm
tech.root: dshow
ms.assetid: f5ebcf96-d008-448e-852b-39bdf1f39c4b
ms.date: 12/05/2018
ms.keywords: GetOutputCurrentType, GetOutputCurrentType method [DirectShow], GetOutputCurrentType method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetOutputCurrentType method, IMediaObject.GetOutputCurrentType, IMediaObject::GetOutputCurrentType, IMediaObjectGetOutputCurrentType, dshow.imediaobject_getoutputcurrenttype, mediaobj/IMediaObject::GetOutputCurrentType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::GetOutputCurrentType
 - mediaobj/IMediaObject::GetOutputCurrentType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.GetOutputCurrentType
---

# IMediaObject::GetOutputCurrentType


## -description

The <code>GetOutputCurrentType</code> method retrieves the media type that was set for an output stream, if any.

## -parameters

### -param dwOutputStreamIndex

Zero-based index of an output stream on the DMO.

### -param pmt [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure allocated by the caller. The method fills the structure with the media type.

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
<dt><b>DMO_E_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
Media type was not set.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The caller must set the media type for the stream before calling this method. To set the media type, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype">IMediaObject::SetOutputType</a> method.

If the method succeeds, call <a href="/windows/desktop/api/dmort/nf-dmort-mofreemediatype">MoFreeMediaType</a> to free the format block.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>