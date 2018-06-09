---
UID: NF:shlwapi.StrRetToStrW
title: StrRetToStrW function
author: windows-sdk-content
description: Takes an STRRET structure returned by IShellFolder::GetDisplayNameOf and returns a pointer to an allocated string containing the display name.
old-location: shell\StrRetToStr.htm
old-project: shell
ms.assetid: 03b0dffb-8ef7-41da-9773-81ed55275802
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: StrRetToStr, StrRetToStr function [Windows Shell], StrRetToStrA, StrRetToStrW, _win32_StrRetToStr, shell.StrRetToStr, shlwapi/StrRetToStr, shlwapi/StrRetToStrA, shlwapi/StrRetToStrW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrRetToStrW (Unicode) and StrRetToStrA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - StrRetToStr
 - StrRetToStrA
 - StrRetToStrW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrRetToStrW function


## -description


Takes an <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure returned by <a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a> and returns a pointer to an allocated string containing the display name.


## -parameters




### -param pstr [in, out]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure. When the function returns, this pointer will no longer be valid.


### -param pidl [in, optional]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. This value can be <b>NULL</b>.


### -param ppsz

TBD




#### - ppszName [out]

Type: <b>LPTSTR*</b>

A pointer to an allocated string containing the result. <b>StrRetToStr</b> allocates memory for this string with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. You should free the string with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/89dab3ee-e9f8-499a-97ec-6fe732315891">StrRetToBuf</a>
 

 

