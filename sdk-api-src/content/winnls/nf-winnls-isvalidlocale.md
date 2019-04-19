---
UID: NF:winnls.IsValidLocale
title: IsValidLocale function (winnls.h)
author: windows-sdk-content
description: Determines if the specified locale is installed or supported on the operating system. For more information, see Locales and Languages.
old-location: intl\isvalidlocale.htm
tech.root: Intl
ms.assetid: b0fb95ff-106d-4269-a696-d39f87fbd745
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsValidLocale, IsValidLocale function [Internationalization for Windows Applications], LCID_INSTALLED, LCID_SUPPORTED, _win32_IsValidLocale, intl.isvalidlocale, winnls/IsValidLocale
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IsValidLocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsValidLocale function


## -description


<p class="CCE_Message">[<b>IsValidLocale</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/cd1b5a4e-7a9c-47a1-9ece-284fce3d5be4">IsValidLocaleName</a> to determine the validity of a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">supplemental locale</a>.]

Determines if the specified locale is installed or supported on the operating system. For more information, see <a href="https://msdn.microsoft.com/8214c00d-4ec6-4597-8088-7819a160f0dc">Locales and Languages</a>.


## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> of the locale to validate. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
<b>Windows Server 2003, Windows XP and Windows 2000:  </b>This locale identifier is not supported.

</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
<b>Windows Server 2003, Windows XP and Windows 2000:  </b>This locale identifier is not supported.

</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
<b>Windows Server 2003, Windows XP and Windows 2000:  </b>This locale identifier is not supported.

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

Flag specifying the validity test to apply to the locale identifier. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LCID_INSTALLED"></a><a id="lcid_installed"></a><dl>
<dt><b>LCID_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Determine if the locale identifier is both supported and installed.

</td>
</tr>
<tr>
<td width="40%"><a id="LCID_SUPPORTED"></a><a id="lcid_supported"></a><dl>
<dt><b>LCID_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Determine if the locale identifier is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x39</dt>
</dl>
</td>
<td width="60%">
Do not use. Instead, use LCID_INSTALLED.

<b>Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP and Windows 2000:  </b>Setting <i>dwFlags</i> to 0x39 is a special case that can behave like LCID_INSTALLED for some locales on some versions of Windows.

</td>
</tr>
</table>
 


## -returns



Returns a nonzero value if the locale identifier passes the specified validity test. The function returns 0 if it does not succeed.




## -remarks



If the LCID_INSTALLED flag is specified and this function returns a nonzero value, the locale identifier is both supported and installed on the operating system. Having an identifier installed implies that the full level of language support is available for the indicated locale. Full support includes code page translation tables, keyboard layouts, fonts, and sorting and locale data.

If LCID_SUPPORTED is specified and this function returns 0, the locale identifier is supported in the release, but not necessarily installed on the operating system.

This function can handle data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a>



<a href="https://msdn.microsoft.com/cd1b5a4e-7a9c-47a1-9ece-284fce3d5be4">IsValidLocaleName</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

