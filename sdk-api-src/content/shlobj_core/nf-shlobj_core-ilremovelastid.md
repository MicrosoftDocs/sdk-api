---
UID: NF:shlobj_core.ILRemoveLastID
title: ILRemoveLastID function (shlobj_core.h)
description: Removes the last SHITEMID structure from an ITEMIDLIST structure.
helpviewer_keywords: ["ILRemoveLastID","ILRemoveLastID function [Windows Shell]","_win32_ILRemoveLastID","shell.ILRemoveLastID","shlobj_core/ILRemoveLastID"]
old-location: shell\ILRemoveLastID.htm
tech.root: shell
ms.assetid: 144df03b-1adc-40c2-a864-3e16bdaf4915
ms.date: 12/05/2018
ms.keywords: ILRemoveLastID, ILRemoveLastID function [Windows Shell], _win32_ILRemoveLastID, shell.ILRemoveLastID, shlobj_core/ILRemoveLastID
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
 - ILRemoveLastID
 - shlobj_core/ILRemoveLastID
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
 - ILRemoveLastID
---

# ILRemoveLastID function


## -description

Removes the last <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure from an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in, out, optional]

Type: <b>PUIDLIST_RELATIVE</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to be shortened. When the function returns, this variable points to the shortened structure.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise.