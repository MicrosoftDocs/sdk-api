---
UID: NF:combaseapi.StringFromIID
title: StringFromIID function (combaseapi.h)
description: Converts an interface identifier into a string of printable characters.
helpviewer_keywords: ["StringFromIID","StringFromIID function [COM]","_com_StringFromIID","com.stringfromiid","combaseapi/StringFromIID"]
old-location: com\stringfromiid.htm
tech.root: com
ms.assetid: 92e59631-0675-4bca-bcd4-a1f83ab6ec8a
ms.date: 12/05/2018
ms.keywords: StringFromIID, StringFromIID function [COM], _com_StringFromIID, com.stringfromiid, combaseapi/StringFromIID
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
 - StringFromIID
 - combaseapi/StringFromIID
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
 - StringFromIID
---

# StringFromIID function


## -description

Converts an interface identifier into a string of printable characters.

## -parameters

### -param rclsid [in]

The interface identifier to be converted.

### -param lplpsz [out]

The address of a pointer variable that receives a pointer to the resulting string. The string that represents <i>rclsid</i> includes enclosing braces.

## -returns

This function can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

The caller is responsible for freeing the memory allocated for the string by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-iidfromstring">IIDFromString</a>