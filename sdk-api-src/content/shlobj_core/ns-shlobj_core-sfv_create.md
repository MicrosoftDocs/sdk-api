---
UID: NS:shlobj_core._SFV_CREATE
title: SFV_CREATE (shlobj_core.h)
description: This structure is used with the SHCreateShellFolderView function.
helpviewer_keywords: ["SFV_CREATE","SFV_CREATE structure [Windows Shell]","_SFV_CREATE","_win32_SFV_CREATE","shell.SFV_CREATE","shlobj_core/SFV_CREATE"]
old-location: shell\SFV_CREATE.htm
tech.root: shell
ms.assetid: c6f3d9a6-5f39-4124-9340-78352f6be117
ms.date: 12/05/2018
ms.keywords: SFV_CREATE, SFV_CREATE structure [Windows Shell], _SFV_CREATE, _win32_SFV_CREATE, shell.SFV_CREATE, shlobj_core/SFV_CREATE
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SFV_CREATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SFV_CREATE
 - shlobj_core/_SFV_CREATE
 - SFV_CREATE
 - shlobj_core/SFV_CREATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SFV_CREATE
---

# SFV_CREATE structure


## -description

This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a> function.

## -struct-fields

### -field cbSize

Type: <b>UINT</b>

The size of the <b>SFV_CREATE</b> structure, in bytes.

### -field pshf

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface of the folder for which to create the view.

### -field psvOuter

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the parent <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface. This parameter may be <b>NULL</b>. This parameter is used only when the view created by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a> is hosted in a common dialog box.

### -field psfvcb

Type: <b><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb">IShellFolderViewCB</a>*</b>

A pointer to the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb">IShellFolderViewCB</a> interface that handles the view's callbacks when various events occur. This parameter may be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a>