---
UID: NE:mfobjects.MF_ATTRIBUTE_SERIALIZE_OPTIONS
title: MF_ATTRIBUTE_SERIALIZE_OPTIONS (mfobjects.h)
description: Defines flags for serializing and deserializing attribute stores.
helpviewer_keywords: ["MF_ATTRIBUTE_SERIALIZE_OPTIONS","MF_ATTRIBUTE_SERIALIZE_OPTIONS enumeration [Media Foundation]","MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF","e4b218d1-185c-483f-b697-19ce8b3a4058","mf.mf_attribute_serialize_options","mfobjects/MF_ATTRIBUTE_SERIALIZE_OPTIONS","mfobjects/MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF"]
old-location: mf\mf_attribute_serialize_options.htm
tech.root: mf
ms.assetid: e4b218d1-185c-483f-b697-19ce8b3a4058
ms.date: 12/05/2018
ms.keywords: MF_ATTRIBUTE_SERIALIZE_OPTIONS, MF_ATTRIBUTE_SERIALIZE_OPTIONS enumeration [Media Foundation], MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF, e4b218d1-185c-483f-b697-19ce8b3a4058, mf.mf_attribute_serialize_options, mfobjects/MF_ATTRIBUTE_SERIALIZE_OPTIONS, mfobjects/MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_ATTRIBUTE_SERIALIZE_OPTIONS
 - mfobjects/MF_ATTRIBUTE_SERIALIZE_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_ATTRIBUTE_SERIALIZE_OPTIONS
---

# MF_ATTRIBUTE_SERIALIZE_OPTIONS enumeration


## -description

Defines flags for serializing and deserializing attribute stores.

## -enum-fields

### -field MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF:0x1

If this flag is set, <b>IUnknown</b> pointers in the attribute store are marshaled to and from the stream. If this flag is absent, <b>IUnknown</b> pointers in the attribute store are not marshaled or serialized.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream">MFDeserializeAttributesFromStream</a>



<a href="/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream">MFSerializeAttributesToStream</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
