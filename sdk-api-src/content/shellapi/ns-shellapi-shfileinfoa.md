---
UID: NS:shellapi._SHFILEINFOA
title: SHFILEINFOA (shellapi.h)
description: Contains information about a file object. (ANSI)
helpviewer_keywords: ["SHFILEINFO","SHFILEINFO structure [Windows Shell]","SHFILEINFOA","_win32_SHFILEINFO","shell.SHFILEINFO","shellapi/SHFILEINFO"]
old-location: shell\SHFILEINFO.htm
tech.root: shell
ms.assetid: 9dbf873a-b447-4579-961e-20f2a64c87fe
ms.date: 12/05/2018
ms.keywords: SHFILEINFO, SHFILEINFO structure [Windows Shell], SHFILEINFOA, _win32_SHFILEINFO, shell.SHFILEINFO, shellapi/SHFILEINFO
req.header: shellapi.h
req.include-header: 
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
req.typenames: SHFILEINFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHFILEINFOA
 - shellapi/_SHFILEINFOA
 - SHFILEINFOA
 - shellapi/SHFILEINFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - SHFILEINFO
 - SHFILEINFOA
---

# SHFILEINFOA structure


## -description

Contains information about a file object.

## -struct-fields

### -field hIcon

Type: <b>HICON</b>

A handle to the icon that represents the file. You are responsible for destroying this handle with <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> when you no longer need it.

### -field iIcon

Type: <b>int</b>

The index of the icon image within the system image list.

### -field dwAttributes

Type: <b>DWORD</b>

An array of values that indicates the attributes of the file object. For information about these values, see the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a> method.

### -field szDisplayName

Type: <b>TCHAR[MAX_PATH]</b>

A string that contains the name of the file as it appears in the Windows Shell, or the path and file name of the file that contains the icon representing the file.

### -field szTypeName

Type: <b>TCHAR[80]</b>

A string that describes the type of file.

## -remarks

This structure is used with the <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a> function.




> [!NOTE]
> The shellapi.h header defines SHFILEINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
