---
UID: NF:shlobj_core.CDefFolderMenu_Create2
title: CDefFolderMenu_Create2 function (shlobj_core.h)
description: Creates a context menu for a selected group of file folder objects.
helpviewer_keywords: ["CDefFolderMenu_Create2","CDefFolderMenu_Create2 function [Windows Shell]","_win32_CDefFolderMenu_Create2","shell.CDefFolderMenu_Create2","shlobj_core/CDefFolderMenu_Create2"]
old-location: shell\CDefFolderMenu_Create2.htm
tech.root: shell
ms.assetid: 7b5e012d-1c8b-42c5-8181-9923fd389fc5
ms.date: 12/05/2018
ms.keywords: CDefFolderMenu_Create2, CDefFolderMenu_Create2 function [Windows Shell], _win32_CDefFolderMenu_Create2, shell.CDefFolderMenu_Create2, shlobj_core/CDefFolderMenu_Create2
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CDefFolderMenu_Create2
 - shlobj_core/CDefFolderMenu_Create2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - CDefFolderMenu_Create2
---

# CDefFolderMenu_Create2 function


## -description

Creates a context menu for a selected group of file folder objects.

## -parameters

### -param pidlFolder [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

An <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure for the parent folder. This value can be <b>NULL</b>.

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window. This value can be <b>NULL</b>.

### -param cidl

Type: <b>UINT</b>

The number of <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures in the array pointed to by <i>apidl</i>.

### -param apidl [in, optional]

Type: <b>PCUITEMID_CHILD_ARRAY*</b>

A pointer to an array of <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures, one for each item that is selected.

### -param psf [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the parent folder's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface. This <b>IShellFolder</b> must support the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface. If it does not, <b>CDefFolderMenu_Create2</b> fails and returns E_NOINTERFACE. This value can be <b>NULL</b>.

### -param pfn [in, optional]

Type: <b><a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfndfmcallback">LPFNDFMCALLBACK</a></b>

The <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfndfmcallback">LPFNDFMCALLBACK</a> callback object. This value can be <b>NULL</b> if the callback object is not needed.

### -param nKeys

Type: <b>UINT</b>

The number of registry keys in the array pointed to by <i>ahkeys</i>.



<div class="alert"><b>Note</b>  The maximum number of registry keys is 16. Callers must enforce this limit as the API does not. Failing to do so can result in memory corruption.</div>
<div> </div>

### -param ahkeys [in, optional]

Type: <b>const HKEY*</b>

A pointer to an array of registry keys that specify the context menu handlers used with the menu's entries. For more information on context menu handlers, see <a href="/windows/desktop/shell/context-menu-handlers">Creating Context Menu Handlers</a>. This array can contain a maximum of 16 registry keys.

### -param ppcm [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a>**</b>

The address of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> interface pointer that, when this function returns successfully, points to the <b>IContextMenu</b> object that represents the context menu.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu">SHCreateDefaultContextMenu</a>