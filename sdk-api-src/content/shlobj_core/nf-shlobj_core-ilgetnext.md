---
UID: NF:shlobj_core.ILGetNext
title: ILGetNext function (shlobj_core.h)
description: Retrieves the next SHITEMID structure in an ITEMIDLIST structure. (ILGetNext)
helpviewer_keywords: ["ILGetNext","ILGetNext function [Windows Shell]","_win32_ILGetNext","shell.ILGetNext","shlobj_core/ILGetNext"]
old-location: shell\ILGetNext.htm
tech.root: shell
ms.assetid: 0b58cc30-fe1a-487c-8f24-f1de54f7730f
ms.date: 12/05/2018
ms.keywords: ILGetNext, ILGetNext function [Windows Shell], _win32_ILGetNext, shell.ILGetNext, shlobj_core/ILGetNext
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
 - ILGetNext
 - shlobj_core/ILGetNext
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
 - ILGetNext
---

# ILGetNext function


## -description

Retrieves the next <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure in an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in, optional]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to a particular <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure in a larger <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -returns

Type: <b>PUIDLIST_RELATIVE</b>

Returns a pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure that follows the one specified by <i>pidl</i>. Returns <b>NULL</b> if <i>pidl</i> points to the last <b>SHITEMID</b> structure.
