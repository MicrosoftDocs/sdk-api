---
UID: NF:shlwapi.StrSpnA
title: StrSpnA function
author: windows-sdk-content
description: Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.
old-location: shell\StrSpn.htm
tech.root: shell
ms.assetid: 1a57da7f-76e7-49f2-aa31-50c224376e95
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: StrSpn, StrSpn function [Windows Shell], StrSpnA, StrSpnW, _win32_StrSpn, shell.StrSpn, shlwapi/StrSpn, shlwapi/StrSpnA, shlwapi/StrSpnW
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
req.unicode-ansi: StrSpnW (Unicode) and StrSpnA (ANSI)
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
 - StrSpn
 - StrSpnA
 - StrSpnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrSpnA function


## -description


Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.


## -parameters




### -param psz [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated string that is to be searched.


### -param pszSet [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated character buffer that contains the set of characters for which to search.


## -returns



Type: <b>int</b>

Returns the length, in characters, of the matching string or zero if no match is found.



