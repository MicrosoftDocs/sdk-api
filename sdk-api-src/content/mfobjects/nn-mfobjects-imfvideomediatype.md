---
UID: NN:mfobjects.IMFVideoMediaType
title: IMFVideoMediaType (mfobjects.h)
description: Represents a description of a video format.
helpviewer_keywords: ["9109b0dd-c44d-41d4-9480-1ca5c667dbd7","IMFVideoMediaType","IMFVideoMediaType interface [Media Foundation]","IMFVideoMediaType interface [Media Foundation]","described","mf.imfvideomediatype","mfobjects/IMFVideoMediaType"]
old-location: mf\imfvideomediatype.htm
tech.root: mf
ms.assetid: 9109b0dd-c44d-41d4-9480-1ca5c667dbd7
ms.date: 12/05/2018
ms.keywords: 9109b0dd-c44d-41d4-9480-1ca5c667dbd7, IMFVideoMediaType, IMFVideoMediaType interface [Media Foundation], IMFVideoMediaType interface [Media Foundation],described, mf.imfvideomediatype, mfobjects/IMFVideoMediaType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoMediaType
 - mfobjects/IMFVideoMediaType
dev_langs:
 - c++
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
---

# IMFVideoMediaType interface


## -description

Represents a description of a video format.

## -inheritance

The <b>IMFVideoMediaType</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>. <b>IMFVideoMediaType</b> also has these types of members:

## -remarks

If the major type of a media type is MFMediaType_Video, you can query the media type object for the <b>IMFVideoMediaType</b> interface.

Applications should avoid using this interface except when a method or function requires an <b>IMFVideoMediaType</b> pointer as a parameter. You can get all of the format information from a video media type through the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface, which <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> inherits.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>
