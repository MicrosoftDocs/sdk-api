---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TranslateNameA function


## -description


Converts a directory service object name from one format to another.


## -parameters




### -param lpAccountName [in]

The name to be translated.


### -param AccountNameFormat [in]

The format of the name to be translated. This parameter is a value from the 
<a href="https://msdn.microsoft.com/1270c412-2fa5-4f5d-a86e-1ab3146c6683">EXTENDED_NAME_FORMAT</a> enumeration type.


### -param DesiredNameFormat [in]

The format of the converted name. This parameter is a value from the 
<a href="https://msdn.microsoft.com/1270c412-2fa5-4f5d-a86e-1ab3146c6683">EXTENDED_NAME_FORMAT</a> enumeration type. It cannot be NameUnknown.


### -param lpTranslatedName [out]

A pointer to a buffer that receives the converted name.


### -param nSize [in, out]

On input, the variable indicates the size of the <i>lpTranslatedName</i> buffer, in <b>TCHARs</b>. On output, the variable returns the size of the returned string, in <b>TCHARs</b>, including the terminating <b>null</b> character. 




If <i>lpTranslated</i> is <b>NULL</b> and <i>nSize</i> is 0, the function succeeds and <i>nSize</i> receives the required buffer size.

If the <i>lpTranslatedName</i> buffer is too small to hold the converted name, the function fails and <i>nSize</i> receives the required buffer size.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>TranslateName</b> fails if it cannot bind to Active Directory on a domain controller.




## -see-also




<a href="https://msdn.microsoft.com/7e083cb5-cf0a-4284-8b54-dac856910c44">Computer Names</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>



<a href="https://msdn.microsoft.com/1270c412-2fa5-4f5d-a86e-1ab3146c6683">EXTENDED_NAME_FORMAT</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System Information Functions</a>
 

 

