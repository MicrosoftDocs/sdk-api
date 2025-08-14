---
UID: NF:combaseapi.StringFromGUID2
title: StringFromGUID2 function (combaseapi.h)
description: Converts a globally unique identifier (GUID) into a string of printable characters.
helpviewer_keywords: ["StringFromGUID2","StringFromGUID2 function [COM]","_com_StringFromGUID2","com.stringfromguid2","combaseapi/StringFromGUID2"]
old-location: com\stringfromguid2.htm
tech.root: com
ms.assetid: 5f437658-b749-416b-805a-2afdac682660
ms.date: 12/05/2018
ms.keywords: StringFromGUID2, StringFromGUID2 function [COM], _com_StringFromGUID2, com.stringfromguid2, combaseapi/StringFromGUID2
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StringFromGUID2
 - combaseapi/StringFromGUID2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - StringFromGUID2
---

# StringFromGUID2 function


## -description

Converts a globally unique identifier (GUID) into a string of printable characters.

## -parameters

### -param rguid [in]

The GUID to be converted.

### -param lpsz [out]

 A pointer to a caller-allocated string variable to receive the resulting string. The string that represents <i>rguid</i> includes enclosing braces.

### -param cchMax [in]

The number of characters available in the <i>lpsz</i> buffer.

## -returns

If the function succeeds, the return value is the number of characters in the returned string, including the null terminator. If the buffer is too small to contain the string, the return value is 0.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-stringfromclsid">StringFromCLSID</a>