---
UID: NN:mfobjects.IMFVideoMediaType
title: IMFVideoMediaType (mfobjects.h)
description: Represents a description of a video format.
old-location: mf\imfvideomediatype.htm
tech.root: medfound
ms.assetid: 9109b0dd-c44d-41d4-9480-1ca5c667dbd7
ms.date: 12/05/2018
ms.keywords: 9109b0dd-c44d-41d4-9480-1ca5c667dbd7, IMFVideoMediaType, IMFVideoMediaType interface [Media Foundation], IMFVideoMediaType interface [Media Foundation],described, mf.imfvideomediatype, mfobjects/IMFVideoMediaType
ms.topic: interface
f1_keywords:
- mfobjects/IMFVideoMediaType
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFVideoMediaType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoMediaType interface


## -description


Represents a description of a video format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMediaType</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>. <b>IMFVideoMediaType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoMediaType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfvideomediatype-getvideoformat">GetVideoFormat</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure that describes the video format. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfvideomediatype-getvideorepresentation">GetVideoRepresentation</a>
</td>
<td align="left" width="63%">
Retrieves an alternative representation of the media type. (Deprecated.)

</td>
</tr>
</table> 


## -remarks



If the major type of a media type is MFMediaType_Video, you can query the media type object for the <b>IMFVideoMediaType</b> interface.

Applications should avoid using this interface except when a method or function requires an <b>IMFVideoMediaType</b> pointer as a parameter. You can get all of the format information from a video media type through the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface, which <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> inherits.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>
 

 

