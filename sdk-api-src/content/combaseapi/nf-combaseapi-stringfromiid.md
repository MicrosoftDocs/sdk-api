---
UID: NF:combaseapi.StringFromIID
title: StringFromIID function
author: windows-sdk-content
description: Converts an interface identifier into a string of printable characters.
old-location: com\stringfromiid.htm
tech.root: com
ms.assetid: 92e59631-0675-4bca-bcd4-a1f83ab6ec8a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: StringFromIID, StringFromIID function [COM], _com_StringFromIID, com.stringfromiid, combaseapi/StringFromIID
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - StringFromIID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- StringFromIID
: 
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



The caller is responsible for freeing the memory allocated for the string by calling the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function. 





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687262(v=VS.85).aspx">IIDFromString</a>
 

 

