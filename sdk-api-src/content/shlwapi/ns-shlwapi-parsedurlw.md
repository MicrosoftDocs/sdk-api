---
UID: NS:shlwapi.tagPARSEDURLW
title: PARSEDURLW (shlwapi.h)
description: Used by the ParseURL function to return the parsed URL. (Unicode)
helpviewer_keywords: ["*PPARSEDURLW","PARSEDURL","PARSEDURL structure [Windows Shell]","PARSEDURLA","PARSEDURLW","PPARSEDURL","PPARSEDURL structure pointer [Windows Shell]","_win32_PARSEDURL","shell.PARSEDURL","shlwapi/PARSEDURL","shlwapi/PARSEDURLA","shlwapi/PARSEDURLW","shlwapi/PPARSEDURL"]
old-location: shell\PARSEDURL.htm
tech.root: shell
ms.assetid: 9092dd7a-ff5b-465f-a808-ef4e0067f540
ms.date: 12/05/2018
ms.keywords: '*PPARSEDURLW, PARSEDURL, PARSEDURL structure [Windows Shell], PARSEDURLA, PARSEDURLW, PPARSEDURL, PPARSEDURL structure pointer [Windows Shell], _win32_PARSEDURL, shell.PARSEDURL, shlwapi/PARSEDURL, shlwapi/PARSEDURLA, shlwapi/PARSEDURLW, shlwapi/PPARSEDURL'
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
targetos: Windows
req.typenames: PARSEDURLW, *PPARSEDURLW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPARSEDURLW
 - shlwapi/tagPARSEDURLW
 - PPARSEDURLW
 - shlwapi/PPARSEDURLW
 - PARSEDURLW
 - shlwapi/PARSEDURLW
dev_langs:
 - c++
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
---

# PARSEDURLW structure


## -description

Used by the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-parseurla">ParseURL</a> function to return the parsed URL.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

[in] The size of the structure, in bytes. The calling application must set this member before calling the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-parseurla">ParseURL</a> function.

### -field pszProtocol

Type: <b>LPCTSTR</b>

[out] A pointer to the beginning of the protocol part of the URL.

### -field cchProtocol

Type: <b>UINT</b>

[out] The number of characters in the URL's protocol section.

### -field pszSuffix

Type: <b>LPCTSTR</b>

[out] A pointer to the section of the URL that follows the protocol and colon (':'). For file URLs, the function also skips the leading "//" characters.

### -field cchSuffix

Type: <b>UINT</b>

[out] The number of characters in the URL's suffix.

### -field nScheme

Type: <b>UINT</b>

[out] A value from the <a href="/windows/desktop/api/shlwapi/ne-shlwapi-url_scheme">URL_SCHEME</a> enumeration that specifies the URL's scheme.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PARSEDURL as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
