---
UID: NF:shlwapi.StrStrNIW
title: StrStrNIW function
author: windows-driver-content
description: Finds the first occurrence of a substring within a string. The comparison is case-insensitive.
old-location: shell\StrStrNIW.htm
old-project: shell
ms.assetid: 743f74f6-a0a6-4c03-b3bf-7f819bbc665f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: StrStrNIW, StrStrNIW function [Windows Shell], _shell_StrStrNIW, shell.StrStrNIW, shlwapi/StrStrNIW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
-	Shell32.dll
-	API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
-	StrStrNIW
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# StrStrNIW function


## -description


Finds the first occurrence of a substring within a string. The comparison is case-insensitive.


## -parameters




### -param pszFirst [in]

Type: <b>PWSTR</b>

A pointer to the null-terminated, Unicode string that is being searched.


### -param pszSrch [in]

Type: <b>PCWSTR</b>

A pointer to the null-terminated, Unicode substring that is being searched for.


### -param cchMax

Type: <b>UINT</b>

The maximum number of characters from the beginning of the searched string in which to search for the substring.


## -returns



Type: <b>PWSTR</b>

Returns the address of the first occurrence of the matching substring if successful, or <b>NULL</b> otherwise.



