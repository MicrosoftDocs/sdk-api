---
UID: NF:winnls.GetNLSVersionEx
title: GetNLSVersionEx function
author: windows-sdk-content
description: Retrieves information about the current version of a specified NLS capability for a locale specified by name.Note  The application should call this function in preference to GetNLSVersion if designed to run only on Windows Vista and later.
old-location: intl\getnlsversionex.htm
old-project: Intl
ms.assetid: 255e6774-eb70-41db-a372-8796166ee8d6
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: GetNLSVersionEx, GetNLSVersionEx function [Internationalization for Windows Applications], _win32_GetNLSVersionEx, intl.getnlsversionex, winnls/GetNLSVersionEx
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetNLSVersionEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNLSVersionEx function


## -description


Retrieves information about the current version of a specified NLS capability for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/09bc53e1-69f4-4a71-82b3-1b1b84a1b84f">GetNLSVersion</a> if designed to run only on Windows Vista and later.</div>
<div> </div>



## -parameters




### -param function [in]

The NLS capability to query. This value must be COMPARE_STRING. See the <a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a> enumeration.


### -param lpLocaleName [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param lpVersionInformation [in, out]

Pointer to an <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure. The application must initialize the <b>dwNLSVersionInfoSize</b> member to <code> sizeof(NLSVERSIONINFOEX)</code>. 

<div class="alert"><b>Note</b>  On Windows Vista and later, the function can alternatively provide version information in an <a href="https://msdn.microsoft.com/6afc8972-373c-4198-ac54-c2a6172b3b39">NLSVERSIONINFO</a> structure.</div>
<div> </div>

## -returns



Returns <b>TRUE</b> if and only if the application has supplied valid values in <i>lpVersionInformation</i>, or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function allows an application such as Active Directory to determine if an NLS change affects the locale used for a particular index table. If it does not, there is no need to re-index the table. For more information, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>. In particular, to tell if a sort version changed and you need to reindex:

<ol>
<li>Use <b>GetNLSVersionEx</b> to retrieve an <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure when doing the original indexing of your data.</li>
<li>Store the following properties with your index to identify the version:<ul>
<li><b>NLSVERSIONINFOEX.dwNLSVersion</b>. This specifies the version of the sorting table you're using.</li>
<li><b>NLSVERSIONINFOEX.dwEffectiveId</b>. This specifies the effective locale of your sort. A custom locale will point to an in-box locale's sort.</li>
<li><b>NLSVERSIONINFOEX.guidCustomVersion</b>. This is a GUID specifying a specific custom sort for custom locales that have them.</li>
</ul>
</li>
<li>When using the index use <b>GetNLSVersionEx</b> to discover the version of your data.</li>
<li>If any of the three properties has changed, the sorting data you're using could return different results and any indexing you have may fail to find records.</li>
<li>If you <u>know</u> that your data doesn't contain invalid Unicode code points (that is, all of your strings passed a call to <a href="https://msdn.microsoft.com/0beb0470-ecdc-4a24-b28c-0738e1df9d49">IsNLSDefinedString</a>) then you may consider them the same if <u>only</u> the low byte of <b>dwNLSVersion</b> changed (the minor version described above).</li>
</ol>
This is covered in more detail in the blog entry <a href="http://go.microsoft.com/fwlink/p/?linkid=151428">"How to tell if the collation version changed"</a> (http://blogs.msdn.com/shawnste/archive/2007/06/01/how-to-tell-if-the-collation-version-changed.aspx).

This function supports <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. If <i>lpLocaleName</i> specifies a supplemental locale, the data retrieved is the correct data for the sort order associated with that supplemental locale.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/09bc53e1-69f4-4a71-82b3-1b1b84a1b84f">GetNLSVersion</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=151428">How to tell if the collation version changed</a>



<a href="https://msdn.microsoft.com/6afc8972-373c-4198-ac54-c2a6172b3b39">NLSVERSIONINFO</a>



<a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a>
 

 

