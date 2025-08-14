---
UID: NF:shlobj_core.SHBindToFolderIDListParent
title: SHBindToFolderIDListParent function (shlobj_core.h)
description: Given a Shell namespace item specified in the form of a folder, and an item identifier list relative to that folder, this function binds to the parent of the namespace item and optionally returns a pointer to the final component of the item identifier list.
helpviewer_keywords: ["SHBindToFolderIDListParent","SHBindToFolderIDListParent function [Windows Shell]","_shell_SHBindToFolderIDListParent","shell.SHBindToFolderIDListParent","shlobj_core/SHBindToFolderIDListParent"]
old-location: shell\SHBindToFolderIDListParent.htm
tech.root: shell
ms.assetid: 72a79d1b-15ed-475e-9ebd-03345579a06a
ms.date: 12/05/2018
ms.keywords: SHBindToFolderIDListParent, SHBindToFolderIDListParent function [Windows Shell], _shell_SHBindToFolderIDListParent, shell.SHBindToFolderIDListParent, shlobj_core/SHBindToFolderIDListParent
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHBindToFolderIDListParent
 - shlobj_core/SHBindToFolderIDListParent
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
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHBindToFolderIDListParent
---

# SHBindToFolderIDListParent function


## -description

Given a Shell namespace item specified in the form of a folder, and an item identifier list relative to that folder, this function binds to the parent of the namespace item and optionally returns a pointer to the final component of the item identifier list.

## -parameters

### -param psfRoot [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to a Shell folder object. If <i>psfRoot</i> is <b>NULL</b>, indicates that the IDList passed is relative to the desktop.

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A PIDL to bind to, relative to <i>psfRoot</i>. If <i>psfRoot</i> is <b>NULL</b>, this is an absolute IDList relative to the desktop folder.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID. This is typically IID_IShellFolder or IID_IShellFolder2, but can be anything supported by the target folder.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>, but can be anything supported by the target folder.

### -param ppidlLast [out, optional]

Type: <b>PCUITEMID_CHILD*</b>

A pointer to the last ID of the <i>pidl</i> parameter, and is a child ID relative to the parent folder returned in <i>ppv</i>. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  Calling the <b>SHBindToFolderIDListParent</b> function is equivalent to calling the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex">SHBindToFolderIDListParentEx</a> function with <b>NULL</b> as the bind context.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex">SHBindToFolderIDListParentEx</a>