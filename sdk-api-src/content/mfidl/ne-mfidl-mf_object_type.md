---
UID: NE:mfidl.MF_OBJECT_TYPE
title: MF_OBJECT_TYPE (mfidl.h)
description: Defines the object types that are created by the source resolver.
helpviewer_keywords: ["MF_OBJECT_BYTESTREAM","MF_OBJECT_INVALID","MF_OBJECT_MEDIASOURCE","MF_OBJECT_TYPE","MF_OBJECT_TYPE enumeration [Media Foundation]","e919ae78-e3a5-42c5-b4e0-186e7e4fe54a","mf.mf_object_type","mfidl/MF_OBJECT_BYTESTREAM","mfidl/MF_OBJECT_INVALID","mfidl/MF_OBJECT_MEDIASOURCE","mfidl/MF_OBJECT_TYPE"]
old-location: mf\mf_object_type.htm
tech.root: mf
ms.assetid: e919ae78-e3a5-42c5-b4e0-186e7e4fe54a
ms.date: 12/05/2018
ms.keywords: MF_OBJECT_BYTESTREAM, MF_OBJECT_INVALID, MF_OBJECT_MEDIASOURCE, MF_OBJECT_TYPE, MF_OBJECT_TYPE enumeration [Media Foundation], e919ae78-e3a5-42c5-b4e0-186e7e4fe54a, mf.mf_object_type, mfidl/MF_OBJECT_BYTESTREAM, mfidl/MF_OBJECT_INVALID, mfidl/MF_OBJECT_MEDIASOURCE, mfidl/MF_OBJECT_TYPE
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MF_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_OBJECT_TYPE
 - mfidl/MF_OBJECT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_OBJECT_TYPE
---

# MF_OBJECT_TYPE enumeration


## -description

Defines the object types that are created by the source resolver.

## -enum-fields

### -field MF_OBJECT_MEDIASOURCE:0

Media source. You can query the object for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface.

### -field MF_OBJECT_BYTESTREAM

Byte stream. You can query the object for the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface.

### -field MF_OBJECT_INVALID

Invalid type.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/source-resolver">Source Resolver</a>
