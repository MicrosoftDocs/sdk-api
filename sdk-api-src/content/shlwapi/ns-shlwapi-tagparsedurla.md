---
UID: NS:shlwapi.tagPARSEDURLA
title: tagPARSEDURLA
author: windows-sdk-content
description: Used by the ParseURL function to return the parsed URL.
old-location: shell\PARSEDURL.htm
tech.root: shell
ms.assetid: 9092dd7a-ff5b-465f-a808-ef4e0067f540
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "*PPARSEDURLA, PARSEDURL, PARSEDURL structure [Windows Shell], PARSEDURLA, PARSEDURLW, PPARSEDURL, PPARSEDURL structure pointer [Windows Shell], _win32_PARSEDURL, shell.PARSEDURL, shlwapi/PARSEDURL, shlwapi/PARSEDURLA, shlwapi/PARSEDURLW, shlwapi/PPARSEDURL, tagPARSEDURLA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PARSEDURLW (Unicode) and PARSEDURLA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - PARSEDURL
 - PARSEDURLA
 - PARSEDURLW
product: Windows
targetos: Windows
req.typenames: PARSEDURLA, *PPARSEDURLA
req.redist: 
---

# tagPARSEDURLA structure


## -description


Used by the <a href="https://msdn.microsoft.com/3d42dad0-b9eb-4e40-afc8-68cb85b27504">ParseURL</a> function to return the parsed URL.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

[in] The size of the structure, in bytes. The calling application must set this member before calling the <a href="https://msdn.microsoft.com/3d42dad0-b9eb-4e40-afc8-68cb85b27504">ParseURL</a> function.


### -field pszProtocol

Type: <b>LPCTSTR</b>

[out] A pointer to the beginning of the protocol part of the URL.


### -field cchProtocol

Type: <b>UINT</b>

The number of characters in the URL's protocol section.


### -field pszSuffix

Type: <b>LPCTSTR</b>

[out] A pointer to the section of the URL that follows the protocol and colon (':'). For file URLs, the function also skips the leading "//" characters.


### -field cchSuffix

Type: <b>UINT</b>

[out] The number of characters in the URL's suffix.


### -field nScheme

Type: <b>UINT</b>

[out] A value from the <a href="https://msdn.microsoft.com/45686920-356d-4dd7-8482-2427854a92ed">URL_SCHEME</a> enumeration that specifies the URL's scheme.

