---
UID: NF:shlobj_core.ILAppendID
title: ILAppendID function (shlobj_core.h)
description: Appends or prepends an SHITEMID structure to an ITEMIDLIST structure.
helpviewer_keywords: ["ILAppendID","ILAppendID function [Windows Shell]","_win32_ILAppendID","shell.ILAppendID","shlobj_core/ILAppendID"]
old-location: shell\ILAppendID.htm
tech.root: shell
ms.assetid: d1bb5993-fe23-42d4-a2c5-8e54e6e37d09
ms.date: 12/05/2018
ms.keywords: ILAppendID, ILAppendID function [Windows Shell], _win32_ILAppendID, shell.ILAppendID, shlobj_core/ILAppendID
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
 - ILAppendID
 - shlobj_core/ILAppendID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - ILAppendID
---

# ILAppendID function


## -description

Appends or prepends an <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in, optional]

Type: <b>PIDLIST_RELATIVE</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure. When the function returns, the <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure specified by <i>pmkid</i> is appended or prepended.

### -param pmkid [in]

Type: <b>LPSHITEMID</b>

A pointer to a <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure to be appended or prepended to <i>pidl</i>.

### -param fAppend

Type: <b>BOOL</b>

Value that is set to <b>TRUE</b> to append <i>pmkid</i> to <i>pidl</i>. Set this value to <b>FALSE</b> to prepend <i>pmkid</i> to <i>pidl</i>.

## -returns

Type: <b>PIDLIST_RELATIVE</b>

Returns the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure specified by <i>pidl</i>, with <i>pmkid</i> appended or prepended. Returns <b>NULL</b> on failure.