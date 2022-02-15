---
UID: NE:mediaobj._DMO_SET_TYPE_FLAGS
title: "_DMO_SET_TYPE_FLAGS (mediaobj.h)"
description: The DMO_SET_TYPE_FLAGS enumeration defines flags for setting the media type on a stream.
helpviewer_keywords: ["DMO_SET_TYPEF_CLEAR","DMO_SET_TYPEF_TEST_ONLY","DMO_SET_TYPE_FLAGS","DMO_SET_TYPE_FLAGSEnumeration","_DMO_SET_TYPE_FLAGS","_DMO_SET_TYPE_FLAGS enumeration [DirectShow]","dshow.dmo_set_type_flags","mediaobj/DMO_SET_TYPEF_CLEAR","mediaobj/DMO_SET_TYPEF_TEST_ONLY","mediaobj/_DMO_SET_TYPE_FLAGS"]
old-location: dshow\dmo_set_type_flags.htm
tech.root: dshow
ms.assetid: e0638668-bbd2-4696-8482-d72438510740
ms.date: 12/05/2018
ms.keywords: DMO_SET_TYPEF_CLEAR, DMO_SET_TYPEF_TEST_ONLY, DMO_SET_TYPE_FLAGS , DMO_SET_TYPE_FLAGSEnumeration, _DMO_SET_TYPE_FLAGS, _DMO_SET_TYPE_FLAGS enumeration [DirectShow], dshow.dmo_set_type_flags, mediaobj/DMO_SET_TYPEF_CLEAR, mediaobj/DMO_SET_TYPEF_TEST_ONLY, mediaobj/_DMO_SET_TYPE_FLAGS
req.header: mediaobj.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DMO_SET_TYPE_FLAGS
 - mediaobj/_DMO_SET_TYPE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_SET_TYPE_FLAGS
---

# _DMO_SET_TYPE_FLAGS enumeration


## -description

The <code>DMO_SET_TYPE_FLAGS</code> enumeration defines flags for setting the media type on a stream.

## -enum-fields

### -field DMO_SET_TYPEF_TEST_ONLY:0x1

Test the media type but do not set it.

### -field DMO_SET_TYPEF_CLEAR:0x2

Clear the media type that was set for the stream.

## -remarks

The DMO_SET_TYPEF_TEST_ONLY and DMO_SET_TYPEF_CLEAR flags are mutually exclusive. Do not set both flags.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype">IMediaObject::SetInputType</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype">IMediaObject::SetOutputType</a>
