---
UID: NF:shlwapi.StrFormatKBSizeA
title: StrFormatKBSizeA function
author: windows-sdk-content
description: Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.
old-location: shell\StrFormatKBSize.htm
tech.root: shell
ms.assetid: 029c2eb8-3bcd-4302-8894-be2dbe430426
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: StrFormatKBSize, StrFormatKBSize function [Windows Shell], StrFormatKBSizeA, StrFormatKBSizeW, _win32_StrFormatKBSize, shell.StrFormatKBSize, shlwapi/StrFormatKBSize, shlwapi/StrFormatKBSizeA, shlwapi/StrFormatKBSizeW
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
req.unicode-ansi: StrFormatKBSizeW (Unicode) and StrFormatKBSizeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrFormatKBSize
 - StrFormatKBSizeA
 - StrFormatKBSizeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- StrFormatKBSizeA
: 
---

# StrFormatKBSizeA function


## -description


Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.


## -parameters




### -param qdw

Type: <b>LONGLONG</b>

The numeric value to be converted.


### -param pszBuf [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the converted number.


### -param cchBuf

Type: <b>UINT</b>

The size of <i>pszBuf</i>, in characters.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to the converted string, or <b>NULL</b> if the conversion fails.




## -remarks



In Windows 10, size is reported in base 10 rather than  base 2. For example, 1 KB is 1000 bytes rather than 1024.




## -see-also




<a href="https://msdn.microsoft.com/244f93cb-0976-4a31-958c-ae0ed81c1dcf">StrFormatByteSizeA</a>



<a href="https://msdn.microsoft.com/00192755-9135-4193-90bc-6e312b294007">StrFormatByteSizeW</a>
 

 

