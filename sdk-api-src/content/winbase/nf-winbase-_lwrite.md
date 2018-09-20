---
UID: NF:winbase._lwrite
title: "_lwrite function"
author: windows-sdk-content
description: Writes data to the specified file.
old-location: winprog\_lwrite.htm
tech.root: devnotes
ms.assetid: 34b875a4-ca45-4f9d-a5be-e6e4d41c68bf
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "_lwrite, _lwrite function [Windows API], winbase/_lwrite, winprog._lwrite"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-2.dll
api_name:
 - _lwrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _lwrite function


## -description


<p class="CCE_Message">[This function is provided for compatibility with 16-bit versions of Windows. New applications should use the <b>WriteFile</b> function.]

Writes data to the specified file.


## -parameters




### -param hFile

A handle to the file that receives the data. This handle is created by <a href="https://msdn.microsoft.com/89e19823-c720-4bfc-95d5-18942573dd94">_lcreat</a>.


### -param lpBuffer

The buffer that contains the data to be added.


### -param uBytes

The number of bytes to write to the file.


## -returns



If the function succeeds, the return value is the number of bytes written to the file. Otherwise, the return value is HFILE_ERROR. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

