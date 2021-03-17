---
UID: NS:oaidl.tagTYPEDESC
title: TYPEDESC (oaidl.h)
description: Describes the type of a variable, the return type of a function, or the type of a function parameter.
helpviewer_keywords: ["TYPEDESC","TYPEDESC structure [Automation]","_oa96_TYPEDESC","automat.typedesc","oaidl/TYPEDESC"]
old-location: automat\typedesc.htm
tech.root: automat
ms.assetid: 45a8c5bf-c776-49da-8517-29055a5e74bc
ms.date: 12/05/2018
ms.keywords: TYPEDESC, TYPEDESC structure [Automation], _oa96_TYPEDESC, automat.typedesc, oaidl/TYPEDESC
req.header: oaidl.h
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
req.typenames: TYPEDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTYPEDESC
 - oaidl/tagTYPEDESC
 - TYPEDESC
 - oaidl/TYPEDESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - TYPEDESC
---

# TYPEDESC structure


## -description

Describes the type of a variable, the return type of a function, or the type of a function parameter.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.lptdesc

 With VT_PTR, the type pointed to.

### -field DUMMYUNIONNAME.lpadesc

With VT_CARRAY...

### -field DUMMYUNIONNAME.hreftype

With VT_USER_DEFINED, this is used to get a TypeInfo for the UDT.

### -field vt

The variant type.

## -remarks

If the variable is VT_SAFEARRAY or VT_PTR, the union portion of the TYPEDESC contains a pointer to a TYPEDESC that specifies the element type.

