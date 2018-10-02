---
UID: NF:shlwapi.StrCpyW
title: StrCpyW function
author: windows-sdk-content
description: Copies one string to another.
old-location: shell\StrCpy.htm
tech.root: Shell
ms.assetid: 83d1a8dc-fc43-4b06-b36c-c9c91d779d25
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: StrCpy, StrCpy function [Windows Shell], StrCpyW, _win32_StrCpy, shell.StrCpy, shlwapi/StrCpy, shlwapi/StrCpyW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCpyW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrCpy
 - StrCpyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrCpyW function


## -description


Copies one string to another.
            
<div class="alert"><b>Note</b>  Do not use. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param psz1 [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the copied string. This string is not guaranteed to be null-terminated.


### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated source string.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to <i>psz1</i>.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The first argument, <i>psz1</i>, must be large enough to hold <i>psz2</i> and the closing '\0', otherwise a buffer overrun may occur. Buffer overruns may lead to a denial of service attack against the application if an access violation occurs. In the worst case, a buffer overrun may allow an attacker to inject executable code into your process, especially if <i>psz1</i> is a stack-based buffer. Consider using one of the following alternatives: <a href="https://msdn.microsoft.com/00c99f3e-106b-46a2-afae-517b32b7a960">StringCbCopy</a>, <a href="https://msdn.microsoft.com/28750482-a0ba-43e1-b433-2c850feef051">StringCbCopyEx</a>, <a href="https://msdn.microsoft.com/4b97de2a-c8bb-423e-8765-a7f20e6fc61c">StringCbCopyN</a>, <a href="https://msdn.microsoft.com/0ef55f41-000c-475a-8227-66df352366fb">StringCbCopyNEx</a>, <a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a>, <a href="https://msdn.microsoft.com/0965b0f6-9588-4944-98d8-3aca3a3029fc">StringCchCopyEx</a>, <a href="https://msdn.microsoft.com/5803c6fa-d1ae-4c3b-8627-162039e8c31f">StringCchCopyN</a>, or <a href="https://msdn.microsoft.com/228ddd78-9747-4a9a-b936-abfba6ff2940">StringCchCopyNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



