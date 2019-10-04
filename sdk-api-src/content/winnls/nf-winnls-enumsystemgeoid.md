---
UID: NF:winnls.EnumSystemGeoID
title: EnumSystemGeoID function (winnls.h)
author: windows-sdk-content
description: Enumerates the geographical location identifiers (type GEOID) that are available on the operating system.
old-location: intl\enumsystemgeoid.htm
tech.root: Intl
ms.assetid: b25d9eb3-baaa-4508-b7d6-e2bccc3c2b77
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumSystemGeoID, EnumSystemGeoID function [Internationalization for Windows Applications], _win32_EnumSystemGeoID, intl.enumsystemgeoid, winnls/EnumSystemGeoID
ms.topic: function
f1_keywords: 
 - "winnls/EnumSystemGeoID"
dev_langs:
 - c++
req.header: winnls.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnumSystemGeoID function


## -description


<p class="CCE_Message">[<b>EnumSystemGeoID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a>.

]

Enumerates the geographical location identifiers (type GEOID) that are available on the operating system.


## -parameters




### -param GeoClass [in]

Geographical location class for which to enumerate the identifiers. At present, only GEOCLASS_NATION is supported. This type causes the function to enumerate all geographical identifiers for nations on the operating system.


### -param ParentGeoId [in]

Reserved. This parameter must be 0.


### -param lpGeoEnumProc [in]

Pointer to the application-defined callback function <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317817(v=vs.85)">EnumGeoInfoProc</a>. The <b>EnumSystemGeoID</b> function makes repeated calls to this callback function until it returns <b>FALSE</b>.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317817(v=vs.85)">EnumGeoInfoProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
 

 

