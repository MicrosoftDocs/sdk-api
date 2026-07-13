---
UID: NF:shlobj_core.ILFindChild
title: ILFindChild function (shlobj_core.h)
description: Determines whether a specified ITEMIDLIST structure is the child of another ITEMIDLIST structure.
helpviewer_keywords: ["ILFindChild","ILFindChild function [Windows Shell]","_win32_ILFindChild","shell.ILFindChild","shlobj_core/ILFindChild"]
old-location: shell\ILFindChild.htm
tech.root: shell
ms.assetid: 4f07e989-ae74-4cf4-b3d9-0f59f2653095
ms.date: 12/05/2018
ms.keywords: ILFindChild, ILFindChild function [Windows Shell], _win32_ILFindChild, shell.ILFindChild, shlobj_core/ILFindChild
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
 - ILFindChild
 - shlobj_core/ILFindChild
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
 - ILFindChild
---

# ILFindChild function


## -description

Determines whether a specified <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure is the child of another <b>ITEMIDLIST</b> structure.

## -parameters

### -param pidlParent [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the parent <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

### -param pidlChild [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the child <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -returns

Type: <b>PUIDLIST_RELATIVE</b>

Returns a pointer to the child's simple <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure if <i>pidlChild</i> is a child of <i>pidlParent</i>. The returned structure consists of <i>pidlChild</i>, minus the <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structures that make up <i>pidlParent</i>. Returns <b>NULL</b> if <i>pidlChild</i> is not a child of <i>pidlParent</i>.

<div class="alert"><b>Note</b>  The returned pointer is a pointer into the existing parent structure. It is an alias for <i>pidlChild</i>. No new memory is allocated in association with the returned pointer. It is not the caller's responsibility to free the returned value.</div>
<div> </div>