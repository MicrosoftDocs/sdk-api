---
UID: NF:combaseapi.StringFromCLSID
title: StringFromCLSID function (combaseapi.h)
author: windows-sdk-content
description: Converts a CLSID into a string of printable characters. Different CLSIDs always convert to different strings.
old-location: com\stringfromclsid.htm
tech.root: com
ms.assetid: 61210ebd-cbf3-4e78-b077-53d2779053eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StringFromCLSID, StringFromCLSID function [COM], _com_StringFromCLSID, com.stringfromclsid, combaseapi/StringFromCLSID
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - StringFromCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StringFromCLSID function


## -description


Converts a CLSID into a string of printable characters. Different CLSIDs always convert to different strings.




## -parameters




### -param rclsid [in]

The CLSID to be converted.


### -param lplpsz [out]

The address of a pointer variable that receives a pointer to the resulting string. The string that represents <i>rclsid</i> includes enclosing braces.


## -returns



This function can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



<b>StringFromCLSID</b> calls the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-stringfromguid2">StringFromGUID2</a> function to convert a globally unique identifier (GUID) into a string of printable characters.

The caller is responsible for freeing the memory allocated for the string by calling the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function. 





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromstring">CLSIDFromString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-stringfromguid2">StringFromGUID2</a>
 

 

