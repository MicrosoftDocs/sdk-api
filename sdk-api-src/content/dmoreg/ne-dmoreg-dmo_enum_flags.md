---
UID: NE:dmoreg.DMO_ENUM_FLAGS
title: DMO_ENUM_FLAGS (dmoreg.h)
description: The DMO_ENUM_FLAGS enumeration defines flags that specify search criteria when enumerating Microsoft DirectX Media Objects (DMOs).
helpviewer_keywords: ["DMO_ENUMF_INCLUDE_KEYED","DMO_ENUM_FLAGS","DMO_ENUM_FLAGS enumeration [DirectShow]","DMO_ENUM_FLAGSEnumeration","dmoreg/DMO_ENUMF_INCLUDE_KEYED","dmoreg/DMO_ENUM_FLAGS","dshow.dmo_enum_flags"]
old-location: dshow\dmo_enum_flags.htm
tech.root: dshow
ms.assetid: ef2be8d8-99d9-4200-8edb-284a5b216814
ms.date: 12/05/2018
ms.keywords: DMO_ENUMF_INCLUDE_KEYED, DMO_ENUM_FLAGS, DMO_ENUM_FLAGS enumeration [DirectShow], DMO_ENUM_FLAGSEnumeration, dmoreg/DMO_ENUMF_INCLUDE_KEYED, dmoreg/DMO_ENUM_FLAGS, dshow.dmo_enum_flags
req.header: dmoreg.h
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
 - DMO_ENUM_FLAGS
 - dmoreg/DMO_ENUM_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dmoreg.h
api_name:
 - DMO_ENUM_FLAGS
---

# DMO_ENUM_FLAGS enumeration


## -description

The <code>DMO_ENUM_FLAGS</code> enumeration defines flags that specify search criteria when enumerating Microsoft DirectX Media Objects (DMOs).

## -enum-fields

### -field DMO_ENUMF_INCLUDE_KEYED:0x00000001

The enumeration should include DMOs whose use is restricted by a software key. If this flag is absent, keyed DMOs are omitted from the enumeration.

## -remarks

A software key enables the developer of a DMO to control who uses the DMO. If a DMO has a software key, applications must unlock the DMO to use it. The method for unlocking the DMO depends on the implementation. Consult the documentation for the particular DMO.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/dmoreg/nf-dmoreg-dmoenum">DMOEnum</a>
