---
UID: NF:shlwapi.StrPBrkW
title: StrPBrkW function
author: windows-driver-content
description: Searches a string for the first occurrence of a character contained in a specified buffer. This search does not include the terminating null character.
old-location: shell\StrPBrk.htm
old-project: shell
ms.assetid: 116c0791-33dd-4c3f-b8a4-a7df91fc5f6a
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: StrPBrk, StrPBrk function [Windows Shell], StrPBrkA, StrPBrkW, _win32_StrPBrk, shell.StrPBrk, shlwapi/StrPBrk, shlwapi/StrPBrkA, shlwapi/StrPBrkW
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
req.unicode-ansi: StrPBrkW (Unicode) and StrPBrkA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
-	StrPBrk
-	StrPBrkA
-	StrPBrkW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrPBrkW function


## -description


Searches a string for the first occurrence of a character contained in a specified buffer. This search does not include the terminating null character.


## -parameters




### -param psz [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to be searched.


### -param pszSet [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated character buffer that contains the characters for which to search.


## -returns



Type: <b>PTSTR</b>

Returns the address in <i>psz</i> of the first occurrence of a character contained in the buffer at <i>pszSet</i>, or <b>NULL</b> if no match is found.



