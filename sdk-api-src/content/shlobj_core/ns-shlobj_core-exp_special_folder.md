---
UID: NS:shlobj_core.EXP_SPECIAL_FOLDER
title: EXP_SPECIAL_FOLDER (shlobj_core.h)
description: Holds an extra data block used by IShellLinkDataList. It holds special folder information.
helpviewer_keywords: ["*LPEXP_SPECIAL_FOLDER","EXP_SPECIAL_FOLDER","EXP_SPECIAL_FOLDER structure [Windows Shell]","LPEXP_SPECIAL_FOLDER","LPEXP_SPECIAL_FOLDER structure pointer [Windows Shell]","_win32_EXP_SPECIAL_FOLDER_str","shell.EXP_SPECIAL_FOLDER_str","shlobj_core/EXP_SPECIAL_FOLDER","shlobj_core/LPEXP_SPECIAL_FOLDER"]
old-location: shell\EXP_SPECIAL_FOLDER_str.htm
tech.root: shell
ms.assetid: e80fa582-8dd1-4924-a3ca-a2ee668653d3
ms.date: 12/05/2018
ms.keywords: '*LPEXP_SPECIAL_FOLDER, EXP_SPECIAL_FOLDER, EXP_SPECIAL_FOLDER structure [Windows Shell], LPEXP_SPECIAL_FOLDER, LPEXP_SPECIAL_FOLDER structure pointer [Windows Shell], _win32_EXP_SPECIAL_FOLDER_str, shell.EXP_SPECIAL_FOLDER_str, shlobj_core/EXP_SPECIAL_FOLDER, shlobj_core/LPEXP_SPECIAL_FOLDER'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: EXP_SPECIAL_FOLDER, *LPEXP_SPECIAL_FOLDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPEXP_SPECIAL_FOLDER
 - shlobj_core/LPEXP_SPECIAL_FOLDER
 - EXP_SPECIAL_FOLDER
 - shlobj_core/EXP_SPECIAL_FOLDER
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
 - EXP_SPECIAL_FOLDER
---

# EXP_SPECIAL_FOLDER structure


## -description

Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>. It holds special folder information.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the <b>EXP_SPECIAL_FOLDER</b> structure.

### -field dwSignature

Type: <b>DWORD</b>

The structure's signature. It should be set to EXP_SPECIAL_FOLDER_SIG.

### -field idSpecialFolder

Type: <b>DWORD</b>

The ID of the special folder that the link points into.

### -field cbOffset

Type: <b>DWORD</b>

The offset into the saved PIDL.

