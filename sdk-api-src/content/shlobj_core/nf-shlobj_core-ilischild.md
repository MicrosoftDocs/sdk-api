---
UID: NF:shlobj_core.ILIsChild
title: ILIsChild function (shlobj_core.h)
description: Verifies whether a pointer to an item identifier list (PIDL) is a child PIDL, which is a PIDL with exactly one SHITEMID.
helpviewer_keywords: ["ILIsChild","ILIsChild function [Windows Shell]","_shell_ILIsChild","shell.ILIsChild","shlobj_core/ILIsChild"]
old-location: shell\ILIsChild.htm
tech.root: shell
ms.assetid: e799fbcf-8254-457a-9d1b-6202dea190c1
ms.date: 12/05/2018
ms.keywords: ILIsChild, ILIsChild function [Windows Shell], _shell_ILIsChild, shell.ILIsChild, shlobj_core/ILIsChild
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
 - ILIsChild
 - shlobj_core/ILIsChild
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - ILIsChild
---

# ILIsChild function


## -description

Verifies whether a pointer to an item identifier list (PIDL) is a child PIDL, which is a PIDL with exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a>.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant, unaligned, relative PIDL that is being checked.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the given PIDL is a child PIDL; otherwise, <b>FALSE</b>.

## -remarks

This function does not guarantee that the PIDL is non-NULL or non-empty.

For use where STRICT_TYPED_ITEMIDS is defined.