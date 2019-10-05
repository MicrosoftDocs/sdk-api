---
UID: NS:shlwapi.tagPARSEDURLW
title: PARSEDURLW (shlwapi.h)
author: windows-sdk-content
description: Used by the ParseURL function to return the parsed URL.
old-location: shell\PARSEDURL.htm
tech.root: shell
ms.assetid: 9092dd7a-ff5b-465f-a808-ef4e0067f540
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPARSEDURLW, PARSEDURL, PARSEDURL structure [Windows Shell], PARSEDURLA, PARSEDURLW, PPARSEDURL, PPARSEDURL structure pointer [Windows Shell], _win32_PARSEDURL, shell.PARSEDURL, shlwapi/PARSEDURL, shlwapi/PARSEDURLA, shlwapi/PARSEDURLW, shlwapi/PPARSEDURL"
ms.topic: struct
f1_keywords: 
 - "shlwapi/PARSEDURL"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: PARSEDURLW, *PPARSEDURLW
req.redist: 
ms.custom: 19H1
---

# PARSEDURLW structure


## -description


Used by the <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-parseurla">ParseURL</a> function to return the parsed URL.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

[in] The size of the structure, in bytes. The calling application must set this member before calling the <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-parseurla">ParseURL</a> function.


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

[out] A value from the <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/ne-shlwapi-url_scheme">URL_SCHEME</a> enumeration that specifies the URL's scheme.

