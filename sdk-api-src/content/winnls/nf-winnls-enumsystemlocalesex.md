---
UID: NF:winnls.EnumSystemLocalesEx
title: EnumSystemLocalesEx function
author: windows-sdk-content
description: Enumerates the locales that are either installed on or supported by an operating system.Note  The application should call this function in preference to EnumSystemLocales if designed to run only on Windows Vista and later.
old-location: intl\enumsystemlocalesex.htm
old-project: Intl
ms.assetid: 74b1b453-66e9-4724-a956-26cea2d7d744
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: EnumSystemLocalesEx, EnumSystemLocalesEx function [Internationalization for Windows Applications], _win32_EnumSystemLocalesEx, intl.enumsystemlocalesex, winnls/EnumSystemLocalesEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - EnumSystemLocalesEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumSystemLocalesEx function


## -description


Enumerates the locales that are either installed on or supported by an operating system.
<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/e6341460-3c4e-4040-8b49-3eb7d279e571">EnumSystemLocales</a> if designed to run only on Windows Vista and later.</div><div> </div>

## -parameters




### -param lpLocaleEnumProcEx [in]

Pointer to an application-defined callback function. The <b>EnumSystemLocalesEx</b> function enumerates locales by making repeated calls to this callback function. For more information, see <a href="https://msdn.microsoft.com/583cc7bc-da1d-4dfc-83f2-2da2b304af62">EnumLocalesProcEx</a>.


### -param dwFlags [in]

Flags identifying the locales to enumerate. The flags can be used singly or combined using a binary OR. If the application specifies 0 for this parameter, the function behaves as for <a href="https://msdn.microsoft.com/40a4ca16-b06c-46be-abe2-bd3e7ed0da4b">LOCALE_ALL</a>.


<ul>
<li>
<a href="https://msdn.microsoft.com/40a4ca16-b06c-46be-abe2-bd3e7ed0da4b">LOCALE_ALL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/92d5d358-7aaa-458d-b044-ee1e63176c66">LOCALE_ALTERNATE_SORTS</a>; see Remarks</li>
<li>
<a href="https://msdn.microsoft.com/2ca39b78-4cbd-4326-95e5-cb233941968f">LOCALE_NEUTRALDATA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/288026bc-4d73-45a7-809a-0385fc678c8d">LOCALE_SUPPLEMENTAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/931ec33d-d1d0-4a6b-aa55-61db2631dd4f">LOCALE_WINDOWS</a>
</li>
</ul>

### -param lParam [in]

An application-provided parameter to be passed to the callback function. This is especially useful for multi-threaded applications.


### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates locales by passing locale names, one at a time, to the application-defined callback function specified by <i>lpLocaleEnumProcEx</i>. Enumeration continues until all installed or supported names have been passed to the callback function or the callback function returns <b>FALSE</b>.

The choices for the <i>dwFlags</i> parameter are different from those for <a href="https://msdn.microsoft.com/e6341460-3c4e-4040-8b49-3eb7d279e571">EnumSystemLocales</a>, which must distinguish between installed and supported locales.

If <i>dwFlags</i> specifies <a href="https://msdn.microsoft.com/92d5d358-7aaa-458d-b044-ee1e63176c66">LOCALE_ALTERNATE_SORTS</a>, the callback function is called for every locale that represents an alternate sort order. For example, Spanish (Spain) defaults to international sort order, but traditional sort order is available for an alternate sort. German (Germany) defaults to dictionary sort order, but there is an alternate phone book sort order available.


#### Examples

An example showing the use of this function can be found in <a href="https://msdn.microsoft.com/0502dba0-a26f-4238-b68e-bb41ef17ff08">NLS: Name-based APIs Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/583cc7bc-da1d-4dfc-83f2-2da2b304af62">EnumLocalesProcEx</a>



<a href="https://msdn.microsoft.com/e6341460-3c4e-4040-8b49-3eb7d279e571">EnumSystemLocales</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

