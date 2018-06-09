---
UID: NF:winnls.ResolveLocaleName
title: ResolveLocaleName function
author: windows-sdk-content
description: Finds a possible locale name match for the supplied name.
old-location: intl\resolvelocalename.htm
old-project: Intl
ms.assetid: 99264b22-3fb5-47e2-b0b9-42a6768e67c1
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ResolveLocaleName, ResolveLocaleName function [Internationalization for Windows Applications], intl.resolvelocalename, winnls/ResolveLocaleName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - ResolveLocaleName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ResolveLocaleName function


## -description


Finds a possible <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a> match for the supplied name.


## -parameters




### -param lpNameToResolve [in, optional]

Pointer to a name to resolve, for example, "en-FJ" for English (Fiji).


### -param lpLocaleName [out, optional]

Pointer to a buffer in which this function retrieves the locale name that is the match for the input name. For example, the match for the name "en-FJ" is "en-US" for English (United States).

<div class="alert"><b>Note</b>  If the function fails, the state of the output buffer is not guaranteed to be accurate. In this case, the application should check the return value and error status set by the function to determine the correct course of action.</div>
<div> </div>

### -param cchLocaleName [in]

Size, in characters, of the buffer indicated by <i>lpLocaleName</i>. The maximum possible length of a locale name, including a terminating null character, is the value of <a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size to supply in this parameter.


## -returns



Returns the size of the buffer containing the locale name, including the terminating null character, if successful.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:
<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
</ul>





## -remarks



The retrieved locale name indicates a specific locale, including language and country/region, even if the input language is neutral. For example, an input of "en" for English (United States) causes the function to retrieve "en-US".

This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application, nor does the return of a valid locale guarantee that it will be valid on another computer. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> Language tags obtained from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace must be converted by  <b>ResolveLocaleName</b> before they can be used with any National Language Support functions.




## -see-also




<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a>
 

 

