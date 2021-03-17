---
UID: NS:shlobj_core._CSFV
title: CSFV (shlobj_core.h)
description: Used with the SHCreateShellFolderViewEx function.
helpviewer_keywords: ["*LPCSFV","CSFV","CSFV structure [Windows Shell]","LPCSFV","LPCSFV structure pointer [Windows Shell]","_CSFV","_win32_CSFV","shell.CSFV","shlobj_core/CSFV","shlobj_core/LPCSFV"]
old-location: shell\CSFV.htm
tech.root: shell
ms.assetid: 9ec22fd4-1562-4ef0-b932-ebbf06082807
ms.date: 12/05/2018
ms.keywords: '*LPCSFV, CSFV, CSFV structure [Windows Shell], LPCSFV, LPCSFV structure pointer [Windows Shell], _CSFV, _win32_CSFV, shell.CSFV, shlobj_core/CSFV, shlobj_core/LPCSFV'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CSFV, *LPCSFV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CSFV
 - shlobj_core/_CSFV
 - LPCSFV
 - shlobj_core/LPCSFV
 - CSFV
 - shlobj_core/CSFV
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
 - CSFV
---

# CSFV structure


## -description

Used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a> function.

## -struct-fields

### -field cbSize

Type: <b>UINT</b>

The size of the <b>CSFV</b> structure, in bytes.

### -field pshf

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object for which to create the view.

### -field psvOuter

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the parent <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface. This parameter can be <b>NULL</b>.

### -field pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

Ignored.

### -field lEvents

Type: <b>LONG</b>

### -field pfnCallback

Type: <b><a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfnviewcallback">LPFNVIEWCALLBACK</a></b>

A pointer to the <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfnviewcallback">LPFNVIEWCALLBACK</a> function used by this folder view to handle callback messages. This parameter can be <b>NULL</b>.

### -field fvm

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a></b>