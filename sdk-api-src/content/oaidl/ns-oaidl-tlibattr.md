---
UID: NS:oaidl.tagTLIBATTR
title: TLIBATTR (oaidl.h)
description: Contains information about a type library. Information from this structure is used to identify the type library and to provide national language support for member names.
helpviewer_keywords: ["*LPTLIBATTR","LPTLIBATTR","LPTLIBATTR structure pointer [Automation]","TLIBATTR","TLIBATTR structure [Automation]","_oa96_TLIBATTR","automat.tlibattr","oaidl/LPTLIBATTR","oaidl/TLIBATTR"]
old-location: automat\tlibattr.htm
tech.root: automat
ms.assetid: 7715a862-1e20-4035-a146-2c9aa134f929
ms.date: 12/05/2018
ms.keywords: '*LPTLIBATTR, LPTLIBATTR, LPTLIBATTR structure pointer [Automation], TLIBATTR, TLIBATTR structure [Automation], _oa96_TLIBATTR, automat.tlibattr, oaidl/LPTLIBATTR, oaidl/TLIBATTR'
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
req.typenames: TLIBATTR, *LPTLIBATTR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTLIBATTR
 - oaidl/tagTLIBATTR
 - LPTLIBATTR
 - oaidl/LPTLIBATTR
 - TLIBATTR
 - oaidl/TLIBATTR
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
 - TLIBATTR
---

# TLIBATTR structure


## -description

Contains information about a type library. Information from this structure is used to identify the type library and to provide national language support for member names.

## -struct-fields

### -field guid

The globally unique identifier.

### -field lcid

The locale identifier.

### -field syskind

The target hardware platform.

### -field wMajorVerNum

The major version number.

### -field wMinorVerNum

The minor version number.

### -field wLibFlags

The library flags.

