---
UID: NF:shobjidl_core.IShellExtInit.Initialize
title: IShellExtInit::Initialize (shobjidl_core.h)
description: Initializes a property sheet extension, shortcut menu extension, or drag-and-drop handler.
helpviewer_keywords: ["IShellExtInit interface [Windows Shell]","Initialize method","IShellExtInit.Initialize","IShellExtInit::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IShellExtInit interface","_win32_IShellExtInit_Initialize","_win32_ishellextinit_win32_ishellextinit_initialize_cpp","shell.IShellExtInit_Initialize","shobjidl_core/IShellExtInit::Initialize"]
old-location: shell\IShellExtInit_Initialize.htm
tech.root: shell
ms.assetid: 1997a32e-562a-4d20-ad09-c40446a8feed
ms.date: 12/05/2018
ms.keywords: IShellExtInit interface [Windows Shell],Initialize method, IShellExtInit.Initialize, IShellExtInit::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IShellExtInit interface, _win32_IShellExtInit_Initialize, _win32_ishellextinit_win32_ishellextinit_initialize_cpp, shell.IShellExtInit_Initialize, shobjidl_core/IShellExtInit::Initialize
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellExtInit::Initialize
 - shobjidl_core/IShellExtInit::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellExtInit.Initialize
---

# IShellExtInit::Initialize


## -description

Initializes a property sheet extension, shortcut menu extension, or drag-and-drop handler.

## -parameters

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that uniquely identifies a folder. For property sheet extensions, this parameter is <b>NULL</b>. For shortcut menu extensions, it is the item identifier list for the folder that contains the item whose shortcut menu is being displayed. For nondefault drag-and-drop menu extensions, this parameter specifies the target folder.

### -param pdtobj [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface object that can be used to retrieve the objects being acted upon.

### -param hkeyProgID [in]

Type: <b>HKEY</b>

The registry key for the file object or folder type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The meanings of some parameters depend on the extension type. For drag-and-drop handlers, the <i>pidlFolder</i> parameter specifies the destination folder (the drop target), the <i>pdtobj</i> parameter identifies the items being dropped, and the <i>hkeyProgID</i> parameter specifies the file type of the destination folder.

For <a href="/windows/desktop/shell/context-menu-handlers">shortcut menu extensions</a>, <i>pdtobj</i> identifies the selected file objects, <i>hkeyProgID</i> identifies the <a href="/windows/desktop/shell/fa-file-types">file type</a> of the object with focus, and <i>pidlFolder</i> is either <b>NULL</b> (for file objects) or specifies the folder for which the shortcut menu is being requested (for folder background shortcut menus).

For property sheet extensions, <i>pidlFolder</i> is <b>NULL</b>, <i>pdtobj</i> identifies the selected file objects, and <i>hkeyProgID</i> specifies the file type of the file object that has the focus.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This is the first method that the Shell calls after it creates an instance of a property sheet extension, shortcut menu extension, or drag-and-drop handler.