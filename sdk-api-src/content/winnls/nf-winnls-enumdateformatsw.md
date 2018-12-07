---
UID: NF:winnls.EnumDateFormatsW
title: EnumDateFormatsW function
author: windows-sdk-content
description: Enumerates the long date, short date, or year/month formats that are available for a specified locale.
old-location: intl\enumdateformats.htm
tech.root: Intl
ms.assetid: 77b5e753-aee9-42d8-a0fa-27b065fc3b20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumDateFormats, EnumDateFormats function [Internationalization for Windows Applications], EnumDateFormatsA, EnumDateFormatsW, _win32_EnumDateFormats, intl.enumdateformats, winnls/EnumDateFormats, winnls/EnumDateFormatsA, winnls/EnumDateFormatsW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDateFormatsW (Unicode) and EnumDateFormatsA (ANSI)
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
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumDateFormats
 - EnumDateFormatsA
 - EnumDateFormatsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumDateFormatsW function


## -description


Enumerates the long date, short date, or year/month formats that are available for a specified locale.
<div class="alert"><b>Note</b>  To receive a calendar identifier in addition to date format information, the application should use the <a href="https://msdn.microsoft.com/523ef50f-722a-48b9-a2ce-20786b7c79e1">EnumDateFormatsEx</a> function. Another reason for preferring this function is that Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales, for interoperability reasons.</div><div> </div><div class="alert"><b>Note</b>  Any application that will be run only on Windows Vista or later should use <a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a> in preference to <b>EnumDateFormats</b>.</div><div> </div>

## -parameters




### -param lpDateFmtEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/622d6f6e-54eb-440b-a426-b2cc533cd8b7">EnumDateFormatsProc</a>.


### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale for which to retrieve date format information. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
</ul>

### -param dwFlags [in]

Flag specifying date formats. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



<div class="alert"><b>Note</b>  This API is being updated to support the May 2019 Japanese era change. If your application supports the Japanese calendar, you should validate that it properly handles the new era. See <a href="https://aka.ms/AA3dzcz">Prepare your application for the Japanese era change</a> for more information.</div>
<div> </div>
For details of operation of this function, see Remarks in <a href="https://msdn.microsoft.com/523ef50f-722a-48b9-a2ce-20786b7c79e1">EnumDateFormatsEx</a>.

<div class="alert"><b>Note</b>  To enumerate the date formats for locales with alternate calendars, the application should use <a href="https://msdn.microsoft.com/523ef50f-722a-48b9-a2ce-20786b7c79e1">EnumDateFormatsEx</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/523ef50f-722a-48b9-a2ce-20786b7c79e1">EnumDateFormatsEx</a>



<a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a>



<a href="https://msdn.microsoft.com/622d6f6e-54eb-440b-a426-b2cc533cd8b7">EnumDateFormatsProc</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

