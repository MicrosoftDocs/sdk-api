---
UID: NF:shlobj_core.ILClone
title: ILClone function (shlobj_core.h)
description: Clones an ITEMIDLIST structure.
helpviewer_keywords: ["ILClone","ILClone function [Windows Shell]","_win32_ILClone","shell.ILClone","shlobj_core/ILClone"]
old-location: shell\ILClone.htm
tech.root: shell
ms.assetid: 90689575-3308-4817-ae8c-380fa5f55c88
ms.date: 12/05/2018
ms.keywords: ILClone, ILClone function [Windows Shell], _win32_ILClone, shell.ILClone, shlobj_core/ILClone
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
 - ILClone
 - shlobj_core/ILClone
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
 - ILClone
---

# ILClone function


## -description

Clones an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to be cloned.

## -returns

Type: <b>PIDLIST_RELATIVE</b>

Returns a pointer to a copy of the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure pointed to by <i>pidl</i>.

## -remarks

When you are finished with the cloned <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure, release it with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> to avoid memory leaks.