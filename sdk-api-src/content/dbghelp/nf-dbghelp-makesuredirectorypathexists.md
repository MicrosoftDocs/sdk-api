---
UID: NF:dbghelp.MakeSureDirectoryPathExists
title: MakeSureDirectoryPathExists function
author: windows-sdk-content
description: Creates all the directories in the specified path, beginning with the root.
old-location: base\makesuredirectorypathexists.htm
tech.root: debug
ms.assetid: 2be9a53a-306a-4b89-a813-0491e8a6e794
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MakeSureDirectoryPathExists, MakeSureDirectoryPathExists function, _win32_makesuredirectorypathexists, base.makesuredirectorypathexists, dbghelp/MakeSureDirectoryPathExists
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# MakeSureDirectoryPathExists function


## -description


Creates all the directories in the specified path, beginning with the root.


## -parameters




### -param DirPath [in]

A valid path name. If the final component of the path is a directory, not a file name, the string must end 
      with a backslash (\) character.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Each directory specified is created, if it does not already exist. If only some of the directories are 
    created, the function will return <b>FALSE</b>.

This function does not support Unicode strings. To specify a Unicode path, use the 
    <a href="https://msdn.microsoft.com/7f44f907-cd12-4156-91c0-76e577ae25f6">SHCreateDirectoryEx</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

