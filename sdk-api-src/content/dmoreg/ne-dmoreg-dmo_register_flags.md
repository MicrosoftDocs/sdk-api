---
UID: NE:dmoreg.DMO_REGISTER_FLAGS
title: DMO_REGISTER_FLAGS (dmoreg.h)
description: The DMO_REGISTER_FLAGS enumeration defines flags that specify registry information for a Microsoft DirectX Media Object (DMO).
helpviewer_keywords: ["DMO_REGISTERF_IS_KEYED","DMO_REGISTER_FLAGS","DMO_REGISTER_FLAGS enumeration [DirectShow]","DMO_REGISTER_FLAGSEnumeration","dmoreg/DMO_REGISTERF_IS_KEYED","dmoreg/DMO_REGISTER_FLAGS","dshow.dmo_register_flags"]
old-location: dshow\dmo_register_flags.htm
tech.root: dshow
ms.assetid: 472be505-a13c-4612-b799-1e9add3ee3fc
ms.date: 12/05/2018
ms.keywords: DMO_REGISTERF_IS_KEYED, DMO_REGISTER_FLAGS, DMO_REGISTER_FLAGS enumeration [DirectShow], DMO_REGISTER_FLAGSEnumeration, dmoreg/DMO_REGISTERF_IS_KEYED, dmoreg/DMO_REGISTER_FLAGS, dshow.dmo_register_flags
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
 - DMO_REGISTER_FLAGS
 - dmoreg/DMO_REGISTER_FLAGS
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
 - DMO_REGISTER_FLAGS
---

# DMO_REGISTER_FLAGS enumeration


## -description

The <code>DMO_REGISTER_FLAGS</code> enumeration defines flags that specify registry information for a Microsoft DirectX Media Object (DMO).

## -enum-fields

### -field DMO_REGISTERF_IS_KEYED:0x00000001

Use of the DMO is restricted by a software key.

## -remarks

A software key enables the developer of a DMO to control who uses the DMO. If a DMO has a software key, applications must unlock the DMO to use it. The method for unlocking the DMO depends on the implementation. Consult the documentation for the particular DMO.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/dmoreg/nf-dmoreg-dmoregister">DMORegister</a>
