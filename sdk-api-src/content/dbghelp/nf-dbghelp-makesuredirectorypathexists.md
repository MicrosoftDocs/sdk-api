---
UID: NF:dbghelp.MakeSureDirectoryPathExists
title: MakeSureDirectoryPathExists function (dbghelp.h)
description: Creates all the directories in the specified path, beginning with the root.
helpviewer_keywords: ["MakeSureDirectoryPathExists","MakeSureDirectoryPathExists function","_win32_makesuredirectorypathexists","base.makesuredirectorypathexists","dbghelp/MakeSureDirectoryPathExists"]
old-location: base\makesuredirectorypathexists.htm
tech.root: Debug
ms.assetid: 2be9a53a-306a-4b89-a813-0491e8a6e794
ms.date: 12/05/2018
ms.keywords: MakeSureDirectoryPathExists, MakeSureDirectoryPathExists function, _win32_makesuredirectorypathexists, base.makesuredirectorypathexists, dbghelp/MakeSureDirectoryPathExists
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - MakeSureDirectoryPathExists
 - dbghelp/MakeSureDirectoryPathExists
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - imagehlp.dll
api_name:
 - MakeSureDirectoryPathExists
---

# MakeSureDirectoryPathExists function


## -description

Creates all the directories in the specified path, beginning with the root.

## -parameters

### -param DirPath [in]

A valid path name. If the final component of the path is a directory, not a file name, the string must end 
      with a backslash (\\) character.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Each directory specified is created, if it does not already exist. If only some of the directories are 
    created, the function will return <b>FALSE</b>.

This function does not support Unicode strings. To specify a Unicode path, use the 
    <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedirectoryexa">SHCreateDirectoryEx</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>