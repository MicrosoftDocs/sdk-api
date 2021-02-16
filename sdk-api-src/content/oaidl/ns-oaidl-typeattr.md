---
UID: NS:oaidl.tagTYPEATTR
title: TYPEATTR (oaidl.h)
description: Contains attributes of a type.
helpviewer_keywords: ["*LPTYPEATTR","LPTYPEATTR","LPTYPEATTR structure pointer [Automation]","TYPEATTR","TYPEATTR structure [Automation]","_oa96_TYPEATTR","automat.typeattr","oaidl/LPTYPEATTR","oaidl/TYPEATTR"]
old-location: automat\typeattr.htm
tech.root: automat
ms.assetid: 00c2b307-b944-44de-a9c7-1165fb27165b
ms.date: 12/05/2018
ms.keywords: '*LPTYPEATTR, LPTYPEATTR, LPTYPEATTR structure pointer [Automation], TYPEATTR, TYPEATTR structure [Automation], _oa96_TYPEATTR, automat.typeattr, oaidl/LPTYPEATTR, oaidl/TYPEATTR'
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
req.typenames: TYPEATTR, *LPTYPEATTR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTYPEATTR
 - oaidl/tagTYPEATTR
 - LPTYPEATTR
 - oaidl/LPTYPEATTR
 - TYPEATTR
 - oaidl/TYPEATTR
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
 - TYPEATTR
---

# TYPEATTR structure


## -description

Contains attributes of a type.

## -struct-fields

### -field guid

The GUID of the type information.

### -field lcid

The locale of member names and documentation strings.

### -field dwReserved

Reserved.

### -field memidConstructor

The constructor ID, or MEMBERID_NIL if none.

### -field memidDestructor

The destructor ID, or MEMBERID_NIL if none.

### -field lpstrSchema

Reserved.

### -field cbSizeInstance

The size of an instance of this type.

### -field typekind

The kind of type.

### -field cFuncs

The number of functions.

### -field cVars

The number of variables or data members.

### -field cImplTypes

The number of implemented interfaces.

### -field cbSizeVft

The size of this type's VTBL.

### -field cbAlignment

The byte alignment for an instance of this type. A value of 0 indicates alignment on the 64K boundary; 1 indicates no special alignment. For other values, <i>n</i> indicates aligned on byte <i>n</i>.

### -field wTypeFlags

The type flags. See <a href="/windows/desktop/api/oaidl/ne-oaidl-typeflags">TYPEFLAGS</a>.

### -field wMajorVerNum

The major version number.

### -field wMinorVerNum

The minor version number.

### -field tdescAlias

If <b>typekind</b> is TKIND_ALIAS, specifies the type for which this type is an alias.

### -field idldescType

The IDL attributes of the described type.