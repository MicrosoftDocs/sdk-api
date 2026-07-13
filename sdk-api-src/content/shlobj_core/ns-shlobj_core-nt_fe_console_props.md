---
UID: NS:shlobj_core.NT_FE_CONSOLE_PROPS
title: NT_FE_CONSOLE_PROPS (shlobj_core.h)
description: Holds an extra data block used by IShellLinkDataList. It holds the console's code page.
helpviewer_keywords: ["*LPNT_FE_CONSOLE_PROPS","LPNT_FE_CONSOLE_PROPS","LPNT_FE_CONSOLE_PROPS structure pointer [Windows Shell]","NT_FE_CONSOLE_PROPS","NT_FE_CONSOLE_PROPS structure [Windows Shell]","_win32_NT_FE_CONSOLE_PROPS_str","shell.NT_FE_CONSOLE_PROPS_str","shlobj_core/LPNT_FE_CONSOLE_PROPS","shlobj_core/NT_FE_CONSOLE_PROPS"]
old-location: shell\NT_FE_CONSOLE_PROPS_str.htm
tech.root: shell
ms.assetid: 2f22676d-2b46-4a94-9517-64d1caeead43
ms.date: 12/05/2018
ms.keywords: '*LPNT_FE_CONSOLE_PROPS, LPNT_FE_CONSOLE_PROPS, LPNT_FE_CONSOLE_PROPS structure pointer [Windows Shell], NT_FE_CONSOLE_PROPS, NT_FE_CONSOLE_PROPS structure [Windows Shell], _win32_NT_FE_CONSOLE_PROPS_str, shell.NT_FE_CONSOLE_PROPS_str, shlobj_core/LPNT_FE_CONSOLE_PROPS, shlobj_core/NT_FE_CONSOLE_PROPS'
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
req.typenames: NT_FE_CONSOLE_PROPS, *LPNT_FE_CONSOLE_PROPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNT_FE_CONSOLE_PROPS
 - shlobj_core/LPNT_FE_CONSOLE_PROPS
 - NT_FE_CONSOLE_PROPS
 - shlobj_core/NT_FE_CONSOLE_PROPS
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
 - NT_FE_CONSOLE_PROPS
---

# NT_FE_CONSOLE_PROPS structure


## -description

Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>. It holds the console's code page.

## -struct-fields

### -field dbh

Type: <b><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header">DATABLOCK_HEADER</a></b>

The <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header">DATABLOCK_HEADER</a> structure with the <b>NT_FE_CONSOLE_PROPS</b> structure's size and signature. The signature for an <b>NT_FE_CONSOLE_PROPS</b> structure is NT_FE_CONSOLE_PROPS_SIG.

### -field DUMMYSTRUCTNAME

### -field uCodePage

Type: <b>UINT</b>

The console's code page.

