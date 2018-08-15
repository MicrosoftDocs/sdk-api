---
UID: NF:winnls.EnumTimeFormatsA
title: EnumTimeFormatsA function
author: windows-sdk-content
description: Enumerates the time formats that are available for a locale specified by identifier.Note  For interoperability reasons, the application should prefer the EnumTimeFormatsEx function to EnumTimeFormats because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use EnumTimeFormatsEx.
old-location: intl\enumtimeformats.htm
old-project: Intl
ms.assetid: ad0fe26f-b915-4903-9335-4b268a889c80
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0, EnumTimeFormats, EnumTimeFormats function [Internationalization for Windows Applications], EnumTimeFormatsA, EnumTimeFormatsW, LOCAL_USE_CP_ACP, TIME_NOSECONDS, _win32_EnumTimeFormats, intl.enumtimeformats, winnls/EnumTimeFormats, winnls/EnumTimeFormatsA, winnls/EnumTimeFormatsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumTimeFormatsW (Unicode) and EnumTimeFormatsA (ANSI)
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
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumTimeFormats
 - EnumTimeFormatsA
 - EnumTimeFormatsW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumTimeFormatsA function


## -description


Enumerates the time formats that are available for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/db2e297e-98db-4e34-b44c-c0ddcddf2a6e">EnumTimeFormatsEx</a> function to <b>EnumTimeFormats</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/db2e297e-98db-4e34-b44c-c0ddcddf2a6e">EnumTimeFormatsEx</a>.</div><div> </div>

## -parameters




### -param lpTimeFmtEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/83d2c214-f36b-42a9-aa58-062992938874">EnumTimeFormatsProc</a>.


### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale for which to retrieve time format information. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

The time format. This parameter can specify a combination of any of the following values.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Use the current user's long time format.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_NOSECONDS"></a><a id="time_noseconds"></a><dl>
<dt><b>TIME_NOSECONDS</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 7 and later</b>: Use the current user's short time format.

<div class="alert"><b>Note</b>  This value will not work with the ANSI version of this function, <b>EnumTimeFormatsA</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="LOCAL_USE_CP_ACP"></a><a id="local_use_cp_acp"></a><dl>
<dt><b>LOCAL_USE_CP_ACP</b></dt>
</dl>
</td>
<td width="60%">
Specified with the ANSI version of this function, <b>EnumTimeFormatsA</b> (not recommended), to use the system default Windows ANSI code page (ACP) instead of the locale code page.

</td>
</tr>
</table>
 


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



The function enumerates the time formats by passing a pointer to a buffer containing a time format to an application-defined callback function. The first value in the enumeration is always the user default (override) value. The function continues enumeration until the last time format is found or the callback function returns <b>FALSE</b>. 


This function can enumerate data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the call can succeed because the system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark ("?"). 
Note that any new values for <i>dwFlags</i> introduced in the future will not work with the ANSI version.




## -see-also




<a href="https://msdn.microsoft.com/db2e297e-98db-4e34-b44c-c0ddcddf2a6e">EnumTimeFormatsEx</a>



<a href="https://msdn.microsoft.com/83d2c214-f36b-42a9-aa58-062992938874">EnumTimeFormatsProc</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

