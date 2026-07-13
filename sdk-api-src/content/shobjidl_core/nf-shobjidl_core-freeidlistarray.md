---
UID: NF:shobjidl_core.FreeIDListArray
title: FreeIDListArray function (shobjidl_core.h)
description: Frees the memory used by a pointer to an item identifier list (PIDL) list array.
helpviewer_keywords: ["FreeIDListArray","FreeIDListArray function [Windows Shell]","_shell_FreeIDListArray","shell.FreeIDListArray","shobjidl_core/FreeIDListArray"]
old-location: shell\FreeIDListArray.htm
tech.root: shell
ms.assetid: 42496da6-452e-45cb-9061-74eba95aff7e
ms.date: 12/05/2018
ms.keywords: FreeIDListArray, FreeIDListArray function [Windows Shell], _shell_FreeIDListArray, shell.FreeIDListArray, shobjidl_core/FreeIDListArray
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
 - FreeIDListArray
 - shobjidl_core/FreeIDListArray
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
 - FreeIDListArray
---

# FreeIDListArray function


## -description

Frees the memory used by a pointer to an item identifier list (PIDL) list array.

## -parameters

### -param ppidls [in]

Type: <b>PIDLIST_RELATIVE*</b>

A pointer to the list of <i>cItems</i> PIDLs, stored as an array.

### -param cItems

Type: <b>UINT</b>

The number of items in the array.

