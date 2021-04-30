---
UID: NF:shobjidl_core.FreeIDListArrayFull
title: FreeIDListArrayFull function (shobjidl_core.h)
description: Releases the memory space for the pointer to an item identifier list (PIDL) array. This releases both the PIDLIST_ABSOLUTEs within the array and the array itself.
helpviewer_keywords: ["FreeIDListArrayFull","FreeIDListArrayFull function [Windows Shell]","_shell_FreeIDListArrayFull","shell.FreeIDListArrayFull","shobjidl_core/FreeIDListArrayFull"]
old-location: shell\FreeIDListArrayFull.htm
tech.root: shell
ms.assetid: ca5e9e02-dcab-4aac-953e-8be0ca8734bc
ms.date: 12/05/2018
ms.keywords: FreeIDListArrayFull, FreeIDListArrayFull function [Windows Shell], _shell_FreeIDListArrayFull, shell.FreeIDListArrayFull, shobjidl_core/FreeIDListArrayFull
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FreeIDListArrayFull
 - shobjidl_core/FreeIDListArrayFull
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FreeIDListArrayFull
---

# FreeIDListArrayFull function


## -description

Releases the memory space for the pointer to an item identifier list (PIDL) array. This releases both the PIDLIST_ABSOLUTEs within the array and the array itself.

## -parameters

### -param ppidls [in]

Type: <b>PIDLIST_ABSOLUTE*</b>

A pointer to the PIDL list, stored as an array of <i>cItems</i> elements.

### -param cItems

Type: <b>UINT</b>

The number of items in the array.

