---
UID: NS:shlobj_core._DROPFILES
title: DROPFILES (shlobj_core.h)
description: Defines the CF_HDROP clipboard format. The data that follows is a double null-terminated list of file names.
helpviewer_keywords: ["*LPDROPFILES","DROPFILES","DROPFILES structure [Windows Shell]","LPDROPFILES","LPDROPFILES structure pointer [Windows Shell]","_DROPFILES","_win32_DROPFILES","shell.DROPFILES","shlobj_core/DROPFILES","shlobj_core/LPDROPFILES"]
old-location: shell\DROPFILES.htm
tech.root: shell
ms.assetid: e1f80529-2151-4ff6-95e0-afff67f2f117
ms.date: 12/05/2018
ms.keywords: '*LPDROPFILES, DROPFILES, DROPFILES structure [Windows Shell], LPDROPFILES, LPDROPFILES structure pointer [Windows Shell], _DROPFILES, _win32_DROPFILES, shell.DROPFILES, shlobj_core/DROPFILES, shlobj_core/LPDROPFILES'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: DROPFILES, *LPDROPFILES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DROPFILES
 - shlobj_core/_DROPFILES
 - LPDROPFILES
 - shlobj_core/LPDROPFILES
 - DROPFILES
 - shlobj_core/DROPFILES
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
 - DROPFILES
---

# DROPFILES structure


## -description

Defines the <a href="/windows/desktop/shell/clipboard">CF_HDROP</a> clipboard format. The data that follows is a double null-terminated list of file names.

## -struct-fields

### -field pFiles

Type: <b>DWORD</b>

The offset of the file list from the beginning of this structure, in bytes.

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The drop point. The coordinates depend on <b>fNC</b>.

### -field fNC

Type: <b>BOOL</b>

A nonclient area flag. If this member is <b>TRUE</b>, <b>pt</b> specifies the screen coordinates of a point in a window's nonclient area. If it is <b>FALSE</b>, <b>pt</b> specifies the client coordinates of a point in the client area.

### -field fWide

Type: <b>BOOL</b>

A value that indicates whether the file contains ANSI or Unicode characters. If the value is zero, the file contains ANSI characters. Otherwise, it contains Unicode characters.