---
UID: NF:winnls.SetCalendarInfoA
title: SetCalendarInfoA function
author: windows-sdk-content
description: Sets an item of locale information for a calendar. For more information, see Date and Calendar.
old-location: intl\setcalendarinfo.htm
tech.root: Intl
ms.assetid: 3599f68f-5b7c-4bf9-9c42-452047c0731f
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: SetCalendarInfo, SetCalendarInfo function [Internationalization for Windows Applications], SetCalendarInfoA, SetCalendarInfoW, _win32_SetCalendarInfo, intl.setcalendarinfo, winnls/SetCalendarInfo, winnls/SetCalendarInfoA, winnls/SetCalendarInfoW
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
req.unicode-ansi: SetCalendarInfoW (Unicode) and SetCalendarInfoA (ANSI)
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - SetCalendarInfo
 - SetCalendarInfoA
 - SetCalendarInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetCalendarInfoA function


## -description


Sets an item of locale information for a calendar. For more information, see <a href="https://msdn.microsoft.com/32772cba-eb30-4cd3-adaf-57fb8425a6d5">Date and Calendar</a>.


## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

<ul>
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
The following custom locale identifiers are also supported.

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
</ul>

### -param Calendar [in]


<a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar identifier</a> for the calendar for which to set information.


### -param CalType [in]

Type of calendar information to set. Only the following CALTYPE values are valid for this function. The CAL_USE_CP_ACP constant is only meaningful for the ANSI version of the function.

<ul>
<li>CAL_USE_CP_ACP</li>
<li>CAL_ITWODIGITYEARMAX</li>
</ul>
The application can specify only one calendar identifier per call to this function. An exception can be made if the application uses the binary OR operator to combine CAL_USE_CP_ACP with any valid CALTYPE value defined in <a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>.


### -param lpCalData [in]

Pointer to a null-terminated calendar information string. The information must be in the format of the specified calendar type.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INTERNAL_ERROR. An unexpected error occurred in the function.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function only affects the user override portion of the calendar settings. It does not set the system defaults.

Calendar information is always passed as a null-terminated Unicode string in the Unicode version of this function, and as a null-terminated ANSI string in the ANSI version. No integers are allowed by this function. Any numeric values must be specified as either Unicode or ANSI text.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 

CAL_ITWODIGITYEARMAX can be used with any calendar, even if the calendar is not supported for the specified locale. To avoid complications, the application should call <a href="https://msdn.microsoft.com/b38abdc9-6c03-4077-9d42-c7cb6d5c66ee">EnumCalendarInfo</a> to ensure that the calendar is supported for the locale of interest.




## -see-also




<a href="https://msdn.microsoft.com/b38abdc9-6c03-4077-9d42-c7cb6d5c66ee">EnumCalendarInfo</a>



<a href="https://msdn.microsoft.com/f32ca0d0-8fa2-41e5-9835-76cf51426c3b">GetCalendarInfo</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

