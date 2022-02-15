---
UID: NE:oaidl.tagSYSKIND
title: SYSKIND (oaidl.h)
description: Identifies the target operating system platform.
helpviewer_keywords: ["SYSKIND","SYSKIND enumeration [Automation]","SYS_MAC","SYS_WIN16","SYS_WIN32","SYS_WIN64","_oa96_SYSKIND","automat.syskind","oaidl/SYSKIND","oaidl/SYS_MAC","oaidl/SYS_WIN16","oaidl/SYS_WIN32","oaidl/SYS_WIN64"]
old-location: automat\syskind.htm
tech.root: automat
ms.assetid: 662048b2-59a8-48ca-9e4f-2f9a5306faa1
ms.date: 12/05/2018
ms.keywords: SYSKIND, SYSKIND enumeration [Automation], SYS_MAC, SYS_WIN16, SYS_WIN32, SYS_WIN64, _oa96_SYSKIND, automat.syskind, oaidl/SYSKIND, oaidl/SYS_MAC, oaidl/SYS_WIN16, oaidl/SYS_WIN32, oaidl/SYS_WIN64
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
req.typenames: SYSKIND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSYSKIND
 - oaidl/tagSYSKIND
 - SYSKIND
 - oaidl/SYSKIND
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
 - SYSKIND
---

# SYSKIND enumeration


## -description

Identifies the target operating system platform.

## -enum-fields

### -field SYS_WIN16:0

The target operating system for the type library is 16-bit Windows. By default, data members are packed.

### -field SYS_WIN32

The target operating system for the type library is 32-bit Windows. By default, data members are naturally aligned (for example, 2-byte integers are aligned on even-byte boundaries; 4-byte integers are aligned on quad-word boundaries, and so on).

### -field SYS_MAC

The target operating system for the type library is Apple Macintosh. By default, all data members are aligned on even-byte boundaries.

### -field SYS_WIN64

The target operating system for the type library is 64-bit Windows.

