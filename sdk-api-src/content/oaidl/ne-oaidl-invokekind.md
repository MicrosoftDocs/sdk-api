---
UID: NE:oaidl.tagINVOKEKIND
title: INVOKEKIND (oaidl.h)
description: Specifies the way a function is invoked.
helpviewer_keywords: ["INVOKEKIND","INVOKEKIND enumeration [Automation]","INVOKE_FUNC","INVOKE_PROPERTYGET","INVOKE_PROPERTYPUT","INVOKE_PROPERTYPUTREF","_oa96_INVOKEKIND","automat.invokekind","oaidl/INVOKEKIND","oaidl/INVOKE_FUNC","oaidl/INVOKE_PROPERTYGET","oaidl/INVOKE_PROPERTYPUT","oaidl/INVOKE_PROPERTYPUTREF"]
old-location: automat\invokekind.htm
tech.root: automat
ms.assetid: df6d392e-88f9-4d22-b257-fb6de8abd289
ms.date: 12/05/2018
ms.keywords: INVOKEKIND, INVOKEKIND enumeration [Automation], INVOKE_FUNC, INVOKE_PROPERTYGET, INVOKE_PROPERTYPUT, INVOKE_PROPERTYPUTREF, _oa96_INVOKEKIND, automat.invokekind, oaidl/INVOKEKIND, oaidl/INVOKE_FUNC, oaidl/INVOKE_PROPERTYGET, oaidl/INVOKE_PROPERTYPUT, oaidl/INVOKE_PROPERTYPUTREF
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
req.typenames: INVOKEKIND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagINVOKEKIND
 - oaidl/tagINVOKEKIND
 - INVOKEKIND
 - oaidl/INVOKEKIND
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
 - INVOKEKIND
---

# INVOKEKIND enumeration


## -description

Specifies the way a function is invoked.

## -enum-fields

### -field INVOKE_FUNC:1

The member is called using a normal function invocation syntax.

### -field INVOKE_PROPERTYGET:2

The function is invoked using a normal property-access syntax.

### -field INVOKE_PROPERTYPUT:4

The function is invoked using a property value assignment syntax. Syntactically, a typical programming language might represent changing a property in the same way as assignment. For example: object.property : = value.

### -field INVOKE_PROPERTYPUTREF:8

The function is invoked using a property reference assignment syntax.

## -remarks

In C, value assignment is written as *pobj1 = *pobj2, while reference assignment is written as pobj1 = pobj2. Other languages have other syntactic conventions. A property or data member can support only a value assignment, a reference assignment, or both. The INVOKEKIND enumeration constants are the same constants that are passed to <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a> to specify the way in which a function is invoked.
