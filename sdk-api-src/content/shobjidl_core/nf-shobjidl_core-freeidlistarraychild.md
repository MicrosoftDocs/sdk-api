---
UID: NF:shobjidl_core.FreeIDListArrayChild
title: FreeIDListArrayChild function (shobjidl_core.h)
description: Releases the memory space for the array of pointers to child item IDs. This releases both the PITEMID_CHILDs within the array and the array itself.
helpviewer_keywords: ["FreeIDListArrayChild","FreeIDListArrayChild function [Windows Shell]","_shell_FreeIDListArrayChild","shell.FreeIDListArrayChild","shobjidl_core/FreeIDListArrayChild"]
old-location: shell\FreeIDListArrayChild.htm
tech.root: shell
ms.assetid: 89abceae-1aed-401d-82ab-57215ec22d00
ms.date: 12/05/2018
ms.keywords: FreeIDListArrayChild, FreeIDListArrayChild function [Windows Shell], _shell_FreeIDListArrayChild, shell.FreeIDListArrayChild, shobjidl_core/FreeIDListArrayChild
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
 - FreeIDListArrayChild
 - shobjidl_core/FreeIDListArrayChild
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
 - FreeIDListArrayChild
---

# FreeIDListArrayChild function


## -description

Releases the memory space for the array of pointers to child item IDs. This releases both the PITEMID_CHILDs within the array and the array itself.

## -parameters

### -param ppidls [in]

Type: <b>PITEMID_CHILD*</b>

A pointer to the PIDL list, stored as an array of <i>cItems</i> elements.

### -param cItems

Type: <b>UINT</b>

The number of items in the array.

