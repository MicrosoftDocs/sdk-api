---
UID: NE:oaidl.tagFUNCKIND
title: FUNCKIND (oaidl.h)
description: Specifies the function type.
helpviewer_keywords: ["FUNCKIND","FUNCKIND enumeration [Automation]","FUNC_DISPATCH","FUNC_NONVIRTUAL","FUNC_PUREVIRTUAL","FUNC_STATIC","FUNC_VIRTUAL","_oa96_FUNCKIND","automat.funckind","oaidl/FUNCKIND","oaidl/FUNC_DISPATCH","oaidl/FUNC_NONVIRTUAL","oaidl/FUNC_PUREVIRTUAL","oaidl/FUNC_STATIC","oaidl/FUNC_VIRTUAL"]
old-location: automat\funckind.htm
tech.root: automat
ms.assetid: da13d9ba-b910-44cc-9926-4368df3f1606
ms.date: 12/05/2018
ms.keywords: FUNCKIND, FUNCKIND enumeration [Automation], FUNC_DISPATCH, FUNC_NONVIRTUAL, FUNC_PUREVIRTUAL, FUNC_STATIC, FUNC_VIRTUAL, _oa96_FUNCKIND, automat.funckind, oaidl/FUNCKIND, oaidl/FUNC_DISPATCH, oaidl/FUNC_NONVIRTUAL, oaidl/FUNC_PUREVIRTUAL, oaidl/FUNC_STATIC, oaidl/FUNC_VIRTUAL
req.header: oaidl.h
req.include-header: OleAuto.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OAIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FUNCKIND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFUNCKIND
 - oaidl/tagFUNCKIND
 - FUNCKIND
 - oaidl/FUNCKIND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OAIdl.h
api_name:
 - FUNCKIND
---

# FUNCKIND enumeration


## -description

Specifies the function type.

## -enum-fields

### -field FUNC_VIRTUAL:0

The function is accessed the same as PUREVIRTUAL, except the function has an implementation.

### -field FUNC_PUREVIRTUAL

The function is accessed through the virtual function table (VTBL), and takes an implicit this pointer.

### -field FUNC_NONVIRTUAL

The function is accessed by static address and takes an implicit this pointer.

### -field FUNC_STATIC

The function is accessed by static address and does not take an implicit this pointer.

### -field FUNC_DISPATCH

The function can be accessed only through <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>.
