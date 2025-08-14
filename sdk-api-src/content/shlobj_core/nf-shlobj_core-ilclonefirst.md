---
UID: NF:shlobj_core.ILCloneFirst
title: ILCloneFirst function (shlobj_core.h)
description: Clones the first SHITEMID structure in an ITEMIDLIST structure.
helpviewer_keywords: ["ILCloneFirst","ILCloneFirst function [Windows Shell]","_win32_ILCloneFirst","shell.ILCloneFirst","shlobj_core/ILCloneFirst"]
old-location: shell\ILCloneFirst.htm
tech.root: shell
ms.assetid: 931df0c7-6acb-4c49-aa2b-464255e97347
ms.date: 12/05/2018
ms.keywords: ILCloneFirst, ILCloneFirst function [Windows Shell], _win32_ILCloneFirst, shell.ILCloneFirst, shlobj_core/ILCloneFirst
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
 - ILCloneFirst
 - shlobj_core/ILCloneFirst
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
 - ILCloneFirst
---

# ILCloneFirst function


## -description

Clones the first <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure in an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that you want to clone.

## -returns

Type: <b>PITEMID_CHILD</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that contains the first <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure from the <b>ITEMIDLIST</b> structure specified by <i>pidl</i>. Returns <b>NULL</b> on failure.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone">ILClone</a>