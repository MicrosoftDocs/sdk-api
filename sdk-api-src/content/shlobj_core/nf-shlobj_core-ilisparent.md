---
UID: NF:shlobj_core.ILIsParent
title: ILIsParent function (shlobj_core.h)
description: Tests whether an ITEMIDLIST structure is the parent of another ITEMIDLIST structure.
helpviewer_keywords: ["ILIsParent","ILIsParent function [Windows Shell]","_win32_ILIsParent","shell.ILIsParent","shlobj_core/ILIsParent"]
old-location: shell\ILIsParent.htm
tech.root: shell
ms.assetid: 638df20b-aa7e-4557-abda-d36b58853aa1
ms.date: 12/05/2018
ms.keywords: ILIsParent, ILIsParent function [Windows Shell], _win32_ILIsParent, shell.ILIsParent, shlobj_core/ILIsParent
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILIsParent
 - shlobj_core/ILIsParent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - ILIsParent
---

# ILIsParent function


## -description

Tests whether an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure is the parent of another <b>ITEMIDLIST</b> structure.

## -parameters

### -param pidl1 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> (PIDL) structure that specifies the parent. This must be an absolute PIDL.

### -param pidl2 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> (PIDL) structure that specifies the child. This must be an absolute PIDL.

### -param fImmediate [in]

Type: <b>BOOL</b>

A Boolean value that is set to <b>TRUE</b> to test for immediate parents of <i>pidl2</i>, or <b>FALSE</b> to test for any parents of <i>pidl2</i>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pidl1</i> is a parent of <i>pidl2</i>. If <i>fImmediate</i> is set to <b>TRUE</b>, the function only returns <b>TRUE</b> if <i>pidl1</i> is the immediate parent of <i>pidl2</i>. Otherwise, the function returns <b>FALSE</b>.