---
UID: NF:winbase.GetDllDirectoryA
title: GetDllDirectoryA function
author: windows-sdk-content
description: Retrieves the application-specific portion of the search path used to locate DLLs for the application.
old-location: base\getdlldirectory.htm
old-project: Dlls
ms.assetid: f892546a-6c48-48f2-8d9a-46e448fffb89
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetDllDirectory, GetDllDirectory function, GetDllDirectoryA, GetDllDirectoryW, base.getdlldirectory, winbase/GetDllDirectory, winbase/GetDllDirectoryA, winbase/GetDllDirectoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDllDirectoryW (Unicode) and GetDllDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - Kernel32Legacy.dll
api_name:
 - GetDllDirectory
 - GetDllDirectoryA
 - GetDllDirectoryW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetDllDirectoryA function


## -description


Retrieves the application-specific portion of the search path used to locate DLLs for the 
   application.


## -parameters




### -param nBufferLength [in]

The size of the output buffer, in characters.


### -param lpBuffer [out]

A pointer to a buffer that receives the application-specific portion of the search path.


## -returns



If the function succeeds, the return value is the length of the string copied to 
       <i>lpBuffer</i>, in characters, not including the terminating null character. If the return 
       value is greater than <i>nBufferLength</i>, it specifies the size of the buffer required for 
       the path.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0502 
    or later. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>



<a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a>
 

 

