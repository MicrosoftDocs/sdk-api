---
UID: NC:winnls.LANGGROUPLOCALE_ENUMPROCW
title: LANGGROUPLOCALE_ENUMPROCW
author: windows-sdk-content
description: An application-defined callback function that processes enumerated language group locale information provided by the EnumLanguageGroupLocales function.
old-location: intl\enumlanguagegrouplocalesproc.htm
tech.root: Intl
ms.assetid: e422c61f-7a97-4f95-8592-22a1eb5f616b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LANGGROUPLOCALE_ENUMPROC, LANGGROUPLOCALE_ENUMPROC callback, LANGGROUPLOCALE_ENUMPROC callback function [Internationalization for Windows Applications], LANGGROUPLOCALE_ENUMPROCA, LANGGROUPLOCALE_ENUMPROCW, _win32_EnumLanguageGroupLocalesProc, intl.enumlanguagegrouplocalesproc, winnls/LANGGROUPLOCALE_ENUMPROC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winnls.h
api_name:
 - LANGGROUPLOCALE_ENUMPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LANGGROUPLOCALE_ENUMPROCW callback function


## -description


An application-defined callback function that processes enumerated language group locale information provided by the <a href="https://msdn.microsoft.com/5a85c6bd-0362-46ff-80be-a198b1259482">EnumLanguageGroupLocales</a> function. The LANGGROUPLOCALE_ENUMPROC type defines a pointer to this callback function. <b>EnumLanguageGroupLocalesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - LanguageGroup [in]

Identifier of the language group. This parameter can have one of the following values:

<ul>
<li>LGRPID_ARABIC</li>
<li>LGRPID_ARMENIAN</li>
<li>LGRPID_BALTIC</li>
<li>LGRPID_CENTRAL_EUROPE</li>
<li>LGRPID_CYRILLIC</li>
<li>LGRPID_GEORGIAN</li>
<li>LGRPID_GREEK</li>
<li>LGRPID_HEBREW</li>
<li>LGRPID_INDIC</li>
<li>LGRPID_JAPANESE</li>
<li>LGRPID_KOREAN
</li>
<li>LGRPID_SIMPLIFIED_CHINESE</li>
<li>LGRPID_TRADITIONAL_CHINESE</li>
<li>LGRPID_THAI</li>
<li>LGRPID_TURKIC</li>
<li>LGRPID_TURKISH</li>
<li>LGRPID_VIETNAMESE</li>
<li>LGRPID_WESTERN_EUROPE</li>
</ul>

#### - Locale [in]


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
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

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

#### - lParam [in]

Application-defined value passed to the <a href="https://msdn.microsoft.com/5a85c6bd-0362-46ff-80be-a198b1259482">EnumLanguageGroupLocales</a> function. This parameter can be used for error checking.


#### - lpLocaleString [in]

Pointer to a buffer containing a null-terminated locale identifier string.


## -returns



Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> otherwise.




## -remarks



An <b>EnumLanguageGroupLocalesProc</b> function can carry out any desired task. The application registers this function by passing its address to the <a href="https://msdn.microsoft.com/5a85c6bd-0362-46ff-80be-a198b1259482">EnumLanguageGroupLocales</a> function.




## -see-also




<a href="https://msdn.microsoft.com/5a85c6bd-0362-46ff-80be-a198b1259482">EnumLanguageGroupLocales</a>



<a href="https://msdn.microsoft.com/8cc2335e-b222-44d9-a966-4b6803639071">EnumSystemLanguageGroups</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

