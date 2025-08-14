---
UID: NF:shlobj_core.ILIsEqual
title: ILIsEqual function (shlobj_core.h)
description: Tests whether two ITEMIDLIST structures are equal in a binary comparison.
helpviewer_keywords: ["ILIsEqual","ILIsEqual function [Windows Shell]","_win32_ILIsEqual","shell.ILIsEqual","shlobj_core/ILIsEqual"]
old-location: shell\ILIsEqual.htm
tech.root: shell
ms.assetid: 139613fc-cd3b-4d5b-b590-096af8f01b62
ms.date: 12/05/2018
ms.keywords: ILIsEqual, ILIsEqual function [Windows Shell], _win32_ILIsEqual, shell.ILIsEqual, shlobj_core/ILIsEqual
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
 - ILIsEqual
 - shlobj_core/ILIsEqual
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
 - Windows.Storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - ILIsEqual
---

# ILIsEqual function


## -description

Tests whether two <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures are equal in a binary comparison.

## -parameters

### -param pidl1 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The first <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

### -param pidl2 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The second <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the two structures are equal, <b>FALSE</b> otherwise.

## -remarks

<b>ILIsEqual</b> performs a binary comparison of the item data. It is possible for two <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures to differ at the binary level while referring to the same item. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">IShellFolder::CompareIDs</a> should be used to perform a non-binary comparison.