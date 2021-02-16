---
UID: NS:rectypes.tagRECO_ATTRS
title: RECO_ATTRS (rectypes.h)
description: Retrieves the attributes of a recognizer or specifies which attributes to use when you search for an installed recognizer.
helpviewer_keywords: ["5ebbb47f-1a11-4e97-8e45-29dbe07fe86d","RECO_ATTRS","RECO_ATTRS structure [Tablet PC]","rectypes/RECO_ATTRS","tablet.reco_attrs"]
old-location: tablet\reco_attrs.htm
tech.root: tablet
ms.assetid: 5ebbb47f-1a11-4e97-8e45-29dbe07fe86d
ms.date: 12/05/2018
ms.keywords: 5ebbb47f-1a11-4e97-8e45-29dbe07fe86d, RECO_ATTRS, RECO_ATTRS structure [Tablet PC], rectypes/RECO_ATTRS, tablet.reco_attrs
req.header: rectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: RECO_ATTRS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRECO_ATTRS
 - rectypes/tagRECO_ATTRS
 - RECO_ATTRS
 - rectypes/RECO_ATTRS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - RECO_ATTRS
---

# RECO_ATTRS structure


## -description

Retrieves the attributes of a recognizer or specifies which attributes to use when you search for an installed recognizer.

## -struct-fields

### -field dwRecoCapabilityFlags

### -field awcVendorName

Vendor who wrote the recognizer.

### -field awcFriendlyName

A human-readable name for the recognizer.

Specify this name when you search for an installed recognizer.

### -field awLanguageId

List of language and sublanguage combinations that the recognizer supports. The list is <b>NULL</b> -terminated.

Specify language identifiers when you search for an installed recognizer if the <i>awcFriendlyName</i> member contains an empty string. Use the MAKELANGID macro to create the language identifiers. If the recognizer does not distinguish between writing styles corresponding to different sublanguages, specify SUBLANG_NEUTRAL for the sublanguage identifier.

## -remarks

The <i>awcFriendlyName</i> parameter may be empty (that is, having the first element set to the null character) when you use this structure as a return value from the <a href="/windows/desktop/api/recapis/nf-recapis-getrecoattributes">GetRecoAttributes Function</a>. Because this is not an error, the return code for <i>awcFriendlyName</i> in <b>GetRecoAttributes Function</b> will be S_OK, and the other fields will contain data.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getrecoattributes">GetRecoAttributes Function</a>