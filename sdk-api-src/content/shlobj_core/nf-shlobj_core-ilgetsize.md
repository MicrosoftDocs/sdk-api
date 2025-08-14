---
UID: NF:shlobj_core.ILGetSize
title: ILGetSize function (shlobj_core.h)
description: Returns the size, in bytes, of an ITEMIDLIST structure.
helpviewer_keywords: ["ILGetSize","ILGetSize function [Windows Shell]","_win32_ILGetSize","shell.ILGetSize","shlobj_core/ILGetSize"]
old-location: shell\ILGetSize.htm
tech.root: shell
ms.assetid: 099d4139-b0ea-42b7-991b-ee04e40994c6
ms.date: 12/05/2018
ms.keywords: ILGetSize, ILGetSize function [Windows Shell], _win32_ILGetSize, shell.ILGetSize, shlobj_core/ILGetSize
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
 - ILGetSize
 - shlobj_core/ILGetSize
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
 - ILGetSize
---

# ILGetSize function


## -description

Returns the size, in bytes, of an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in, optional]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -returns

Type: <b>UINT</b>

The size of the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure specified by <i>pidl</i>, in bytes.