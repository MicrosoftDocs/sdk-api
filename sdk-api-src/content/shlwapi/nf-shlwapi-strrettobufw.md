---
UID: NF:shlwapi.StrRetToBufW
title: StrRetToBufW function
author: windows-sdk-content
description: Converts an STRRET structure returned by IShellFolder::GetDisplayNameOf to a string, and places the result in a buffer.
old-location: shell\StrRetToBuf.htm
old-project: shell
ms.assetid: 89dab3ee-e9f8-499a-97ec-6fe732315891
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: StrRetToBuf, StrRetToBuf function [Windows Shell], StrRetToBufA, StrRetToBufW, _win32_StrRetToBuf, shell.StrRetToBuf, shlwapi/StrRetToBuf, shlwapi/StrRetToBufA, shlwapi/StrRetToBufW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrRetToBufW (Unicode) and StrRetToBufA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - StrRetToBuf
 - StrRetToBufA
 - StrRetToBufW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrRetToBufW function


## -description


Converts an <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure returned by <a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a> to a string, and places the result in a buffer.


## -parameters




### -param pstr [in, out]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure. When the function returns, this pointer will no longer be valid.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param pszBuf [out]

Type: <b>LPTSTR</b>

A buffer to hold the display name. It will be returned as a null-terminated string. If <i>cchBuf</i> is too small, the name will be truncated to fit.


### -param cchBuf [in]

Type: <b>UINT</b>

The size of <i>pszBuf</i>, in characters. If <i>cchBuf</i> is too small, the string will be truncated to fit.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <b>uType</b> member of the structure pointed to by <i>pstr</i> is set to <b>STRRET_WSTR</b>, the <b>pOleStr</b> member of that structure will be freed on return.




## -see-also




<a href="https://msdn.microsoft.com/03b0dffb-8ef7-41da-9773-81ed55275802">StrRetToStr</a>



<a href="https://msdn.microsoft.com/a816fb5f-8320-4b63-a85d-dd4c59596ead">StrRetToStrN</a>
 

 

