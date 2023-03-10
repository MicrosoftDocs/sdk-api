---
UID: NS:shlobj.SHCOLUMNINIT
title: SHCOLUMNINIT (shlobj.h)
description: Passes initialization information to IColumnProvider::Initialize.
helpviewer_keywords: ["*LPSHCOLUMNINIT","LPSHCOLUMNINFO","LPSHCOLUMNINFO structure pointer [Windows Shell]","SHCOLUMNINIT","SHCOLUMNINIT structure [Windows Shell]","_win32_SHCOLUMNINIT_str","shell.SHCOLUMNINIT_str","shlobj/LPSHCOLUMNINFO","shlobj/SHCOLUMNINIT"]
old-location: shell\SHCOLUMNINIT_str.htm
tech.root: shell
ms.assetid: eebe47c8-b3ee-4316-b578-5404ed8f7920
ms.date: 12/05/2018
ms.keywords: '*LPSHCOLUMNINIT, LPSHCOLUMNINFO, LPSHCOLUMNINFO structure pointer [Windows Shell], SHCOLUMNINIT, SHCOLUMNINIT structure [Windows Shell], _win32_SHCOLUMNINIT_str, shell.SHCOLUMNINIT_str, shlobj/LPSHCOLUMNINFO, shlobj/SHCOLUMNINIT'
req.header: shlobj.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHCOLUMNINIT, *LPSHCOLUMNINIT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPSHCOLUMNINIT
 - shlobj/LPSHCOLUMNINIT
 - SHCOLUMNINIT
 - shlobj/SHCOLUMNINIT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - SHCOLUMNINIT
---

# SHCOLUMNINIT structure


## -description

Passes initialization information to <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize">IColumnProvider::Initialize</a>.

## -struct-fields

### -field dwFlags

Type: <b>ULONG</b>

Initialization flags. Reserved. Set to <b>NULL</b>

### -field dwReserved

Type: <b>ULONG</b>

Reserved. Set to <b>NULL</b>.

### -field wszFolder

Type: <b>WCHAR[MAX_PATH]</b>

A pointer to a null-terminated Unicode string with a fully qualified folder path. The string will be empty if multiple folders are specified.

