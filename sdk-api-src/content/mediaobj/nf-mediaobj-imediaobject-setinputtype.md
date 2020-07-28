---
UID: NF:mediaobj.IMediaObject.SetInputType
title: IMediaObject::SetInputType (mediaobj.h)
description: The SetInputType method sets the media type on an input stream, or tests whether a media type is acceptable.
helpviewer_keywords: ["IMediaObject interface [DirectShow]","SetInputType method","IMediaObject.SetInputType","IMediaObject::SetInputType","IMediaObjectSetInputType","SetInputType","SetInputType method [DirectShow]","SetInputType method [DirectShow]","IMediaObject interface","dshow.imediaobject_setinputtype","mediaobj/IMediaObject::SetInputType"]
old-location: dshow\imediaobject_setinputtype.htm
tech.root: dshow
ms.assetid: 6b466fe4-97a0-46f9-9e4b-461ee66095f1
ms.date: 12/05/2018
ms.keywords: IMediaObject interface [DirectShow],SetInputType method, IMediaObject.SetInputType, IMediaObject::SetInputType, IMediaObjectSetInputType, SetInputType, SetInputType method [DirectShow], SetInputType method [DirectShow],IMediaObject interface, dshow.imediaobject_setinputtype, mediaobj/IMediaObject::SetInputType
f1_keywords:
- mediaobj/IMediaObject.SetInputType
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
- IMediaObject.SetInputType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaObject::SetInputType


## -description



The <code>SetInputType</code> method sets the media type on an input stream, or tests whether a media type is acceptable.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param pmt [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure that specifies the media type.


### -param dwFlags

Bitwise combination of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_set_type_flags">DMO_SET_TYPE_FLAGS</a> enumeration.


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
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_TYPE_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
Media type was not accepted

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Media type is not acceptable

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Media type was set successfully, or is acceptable

</td>
</tr>
</table>
 




## -remarks



Call this method to test, set, or clear the media type on an input stream:

<ul>
<li>To test the media type without setting it, use the DMO_SET_TYPEF_TEST_ONLY flag. If the media type is not acceptable, the method returns S_FALSE.</li>
<li>To set the media type, set <i>dwFlags</i> to zero. If the media type is not acceptable, the method returns DMO_E_TYPE_NOT_ACCEPTED.</li>
<li>To clear the current media type (if any), use the DMO_SET_TYPEF_CLEAR flag and set <i>pmt</i> to <b>NULL</b>. When the method returns, the stream no longer has a media type. The DMO cannot process samples until the application sets a new media type.</li>
</ul>
The media types that are currently set on other streams can affect whether the media type is acceptable.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>
 

 

