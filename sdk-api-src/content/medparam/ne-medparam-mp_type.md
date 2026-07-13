---
UID: NE:medparam._MP_Type
title: MP_TYPE (medparam.h)
description: The MP_TYPE enumeration specifies the data type for a parameter.
helpviewer_keywords: ["MPT_BOOL","MPT_ENUM","MPT_FLOAT","MPT_INT","MPT_MAX","MP_TYPE","MP_TYPE","MP_TYPE enumeration [DirectShow]","MP_TYPEEnumeration","dshow.mp_type","medparam/MPT_BOOL","medparam/MPT_ENUM","medparam/MPT_FLOAT","medparam/MPT_INT","medparam/MPT_MAX","medparam/MP_TYPE"]
old-location: dshow\mp_type.htm
tech.root: dshow
ms.assetid: 9c8851c7-1a72-4dfd-ba2f-e64d8e22f6dc
ms.date: 4/26/2023
ms.keywords: MPT_BOOL, MPT_ENUM, MPT_FLOAT, MPT_INT, MPT_MAX, MP_TYPE, MP_TYPE , MP_TYPE enumeration [DirectShow], MP_TYPEEnumeration, dshow.mp_type, medparam/MPT_BOOL, medparam/MPT_ENUM, medparam/MPT_FLOAT, medparam/MPT_INT, medparam/MPT_MAX, medparam/MP_TYPE
req.header: medparam.h
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
req.typenames: MP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MP_Type
 - medparam/_MP_Type
 - MP_TYPE
 - medparam/MP_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Medparam.h
api_name:
 - MP_TYPE
---

# MP_TYPE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>MP_TYPE</code> enumeration specifies the data type for a parameter.

## -enum-fields

### -field MPT_INT:0

Value is a signed 32-bit integer.

### -field MPT_FLOAT

Value is a 32-bit IEEE floating-point value.

### -field MPT_BOOL

Value is Boolean. Use the following constants for Boolean parameters:

### -field MPT_ENUM

Value is taken from a set of consecutive integers.

### -field MPT_MAX

Reserved.

## -remarks

To reduce type conversions at run time, all parameters have 32-bit float values, defined as type <b>MP_DATA</b>. The members of this enumeration specify how a given parameter should be interpreted.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/previous-versions/windows/desktop/api/medparam/ns-medparam-mp_paraminfo">MP_PARAMINFO</a>
