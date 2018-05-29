---
UID: NF:winnls.GetNLSVersion
title: GetNLSVersion function
author: windows-sdk-content
description: Retrieves information about the current version of a specified NLS capability for a locale specified by identifier.Note  For interoperability reasons, the application should prefer the GetNLSVersionEx function to GetNLSVersion because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. This recommendation applies especially to custom locales, for which GetNLSVersionEx retrieves enough information to determine if sort behavior has changed. Any application that runs only on Windows Vista and later should use GetNLSVersionEx or at least pass the NLSVERSIONINFOEX structure when calling GetNLSVersion to obtain additional sorting versioning data.
old-location: intl\getnlsversion.htm
old-project: Intl
ms.assetid: 09bc53e1-69f4-4a71-82b3-1b1b84a1b84f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetNLSVersion, GetNLSVersion function [Internationalization for Windows Applications], _win32_GetNLSVersion, intl.getnlsversion, winnls/GetNLSVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Localization-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-l1-2-0.dll
-	API-MS-Win-Core-Localization-l1-2-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
-	GetNLSVersion
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNLSVersion function


## -description


Retrieves information about the current version of a specified NLS capability for a locale specified by identifier.<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a> function to <b>GetNLSVersion</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. This recommendation applies especially to custom locales, for which <b>GetNLSVersionEx</b> retrieves enough information to determine if sort behavior has changed. Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a> or at least pass the <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure when calling <b>GetNLSVersion</b> to obtain additional sorting versioning data.</div>
<div> </div>



## -parameters




### -param Function [in]

The NLS capability to query. This value must be COMPARE_STRING. See the <a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a> enumeration.


### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

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

### -param lpVersionInformation [in, out]

Pointer to an <a href="https://msdn.microsoft.com/6afc8972-373c-4198-ac54-c2a6172b3b39">NLSVERSIONINFO</a> structure. The application must initialize the <b>dwNLSVersionInfoSize</b> member to <code>sizeof(NLSVERSIONINFO)</code>.

<div class="alert"><b>Note</b>  On Windows Vista and later, the function can alternatively provide version information in an <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure.</div>
<div> </div>

## -returns



Returns <b>TRUE</b> if and only if the application has supplied valid values in <i>lpVersionInformation</i>, or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table. If it does not, there is no need to re-index the table. For more information, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/6afc8972-373c-4198-ac54-c2a6172b3b39">NLSVERSIONINFO</a>



<a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a>
 

 

