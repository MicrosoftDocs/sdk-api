---
UID: NF:winnls.EnumSystemGeoID
title: EnumSystemGeoID function
author: windows-sdk-content
description: Enumerates the geographical location identifiers (type GEOID) that are available on the operating system.
old-location: intl\enumsystemgeoid.htm
old-project: Intl
ms.assetid: b25d9eb3-baaa-4508-b7d6-e2bccc3c2b77
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: EnumSystemGeoID, EnumSystemGeoID function [Internationalization for Windows Applications], _win32_EnumSystemGeoID, intl.enumsystemgeoid, winnls/EnumSystemGeoID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - EnumSystemGeoID
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumSystemGeoID function


## -description


<p class="CCE_Message">[<b>EnumSystemGeoID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a>.

]

Enumerates the geographical location identifiers (type GEOID) that are available on the operating system.


## -parameters




### -param GeoClass [in]

Geographical location class for which to enumerate the identifiers. At present, only GEOCLASS_NATION is supported. This type causes the function to enumerate all geographical identifiers for nations on the operating system.


### -param ParentGeoId [in]

Reserved. This parameter must be 0.


### -param lpGeoEnumProc [in]

Pointer to the application-defined callback function <a href="https://msdn.microsoft.com/a906ecd3-9d9f-4d70-9571-095a224f3b5f">EnumGeoInfoProc</a>. The <b>EnumSystemGeoID</b> function makes repeated calls to this callback function until it returns <b>FALSE</b>.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a906ecd3-9d9f-4d70-9571-095a224f3b5f">EnumGeoInfoProc</a>



<a href="https://msdn.microsoft.com/0CB7AE4E-F48A-49A6-A5E8-F151D38CE11E">EnumSystemGeoNames</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

