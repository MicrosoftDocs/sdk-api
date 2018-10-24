---
UID: NF:shlwapi.StrCpyNW
title: StrCpyNW function
author: windows-sdk-content
description: Copies a specified number of characters from the beginning of one string to another.Note  Do not use this function or the StrNCpy macro.
old-location: shell\StrCpyN.htm
tech.root: shell
ms.assetid: 7e21414d-0d82-40b9-b32f-5eaf351166da
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: StrCpyN, StrCpyN function [Windows Shell], StrCpyNW, _win32_StrCpyN, shell.StrCpyN, shlwapi/StrCpyN, shlwapi/StrCpyNW
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
req.unicode-ansi: StrCpyNW (Unicode)
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
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrCpyN
 - StrCpyNW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrCpyNW function


## -description


Copies a specified number of characters from the beginning of one string to another.
<div class="alert"><b>Note</b>  Do not use this function or the <b>StrNCpy</b> macro. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param pszDst [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the copied string. This buffer must be of sufficient size to hold the copied characters. This string is not guaranteed to be null-terminated.


### -param pszSrc [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated source string.


### -param cchMax

Type: <b>int</b>

The number of characters to be copied, including the terminating null character.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to <i>pszDst</i>.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The copied string is not guaranteed to be null-terminated.  Consider using one of the following alternatives. <a href="https://msdn.microsoft.com/00c99f3e-106b-46a2-afae-517b32b7a960">StringCbCopy</a>, <a href="https://msdn.microsoft.com/28750482-a0ba-43e1-b433-2c850feef051">StringCbCopyEx</a>, <a href="https://msdn.microsoft.com/4b97de2a-c8bb-423e-8765-a7f20e6fc61c">StringCbCopyN</a>, <a href="https://msdn.microsoft.com/0ef55f41-000c-475a-8227-66df352366fb">StringCbCopyNEx</a>, <a href="https://msdn.microsoft.com/9cbf6ce6-ef45-4bb9-bc1f-a55db399d34f">StringCchCopy</a>, <a href="https://msdn.microsoft.com/0965b0f6-9588-4944-98d8-3aca3a3029fc">StringCchCopyEx</a>, <a href="https://msdn.microsoft.com/5803c6fa-d1ae-4c3b-8627-162039e8c31f">StringCchCopyN</a>, <a href="https://msdn.microsoft.com/228ddd78-9747-4a9a-b936-abfba6ff2940">StringCchCopyNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



