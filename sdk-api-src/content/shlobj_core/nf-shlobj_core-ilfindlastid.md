---
UID: NF:shlobj_core.ILFindLastID
title: ILFindLastID function (shlobj_core.h)
description: Returns a pointer to the last SHITEMID structure in an ITEMIDLIST structure.
helpviewer_keywords: ["ILFindLastID","ILFindLastID function [Windows Shell]","_win32_ILFindLastID","shell.ILFindLastID","shlobj_core/ILFindLastID"]
old-location: shell\ILFindLastID.htm
tech.root: shell
ms.assetid: 877029b7-a2fb-42c2-98a1-0eb6f229f1d9
ms.date: 12/05/2018
ms.keywords: ILFindLastID, ILFindLastID function [Windows Shell], _win32_ILFindLastID, shell.ILFindLastID, shlobj_core/ILFindLastID
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
 - ILFindLastID
 - shlobj_core/ILFindLastID
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
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - ILFindLastID
---

# ILFindLastID function


## -description

Returns a pointer to the last <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure in an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -returns

Type: <b>PUITEMID_CHILD</b>

A pointer to the last <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure in <i>pidl</i>.

## -remarks

This function does not clone the last item, so you do not have to call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> to release the returned pointer.