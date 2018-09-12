---
UID: NF:winnls.GetProcessPreferredUILanguages
title: GetProcessPreferredUILanguages function
author: windows-sdk-content
description: Retrieves the process preferred UI languages. For more information, see User Interface Language Management.
old-location: intl\getprocesspreferreduilanguages.htm
tech.root: Intl
ms.assetid: 115fd1f4-39ae-4c69-aa42-606617a989aa
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: GetProcessPreferredUILanguages, GetProcessPreferredUILanguages function [Internationalization for Windows Applications], MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, intl.getprocesspreferreduilanguages, winnls/GetProcessPreferredUILanguages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - GetProcessPreferredUILanguages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetProcessPreferredUILanguages function


## -description


Retrieves the process preferred UI languages. For more information, see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a>.


## -parameters




### -param dwFlags [in]

Flags identifying the language format to use for the process preferred UI languages. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_ID"></a><a id="mui_language_id"></a><dl>
<dt><b>MUI_LANGUAGE_ID</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the language strings in <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the language strings in <a href="https://msdn.microsoft.com/e8c54168-22b3-435e-b19a-9b34adcdb018">language name</a> format.

</td>
</tr>
</table>
 


### -param pulNumLanguages [out]

Pointer to the number of languages retrieved in <i>pwszLanguagesBuffer</i>.


### -param pwszLanguagesBuffer [out, optional]

Optional. Pointer to a double null-terminated multi-string buffer in which the function retrieves an ordered, null-delimited list in preference order, starting with the most preferable. 

Alternatively if this parameter is set to <b>NULL</b> and <i>pcchLanguagesBuffer</i> is set to 0, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>. The required size includes the two null characters.


### -param pcchLanguagesBuffer [in, out]

Pointer to the size, in characters, for the language buffer indicated by <i>pwszLanguagesBuffer</i>. On successful return from the function, the parameter contains the size of the retrieved language buffer.

Alternatively if this parameter is set to 0 and <i>pwszLanguagesBuffer</i> is set to <b>NULL</b>, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>
If the process preferred UI language list is empty or if the languages specified for the process are not valid, the function succeeds and returns an empty multistring in <i>pwszLanguagesBuffer</i> and 2 in the <i>pcchLanguagesBuffer</i> parameter.





## -remarks



Depending on the flags specified by the application, this function can retrieve a list consisting of the process preferred UI languages. If it encounters a duplicate language, the function only retrieves the first instance of the duplicated language.

When MUI_LANGUAGE_ID is specified, the language strings retrieved will be hexadecimal language identifiers 

that do not include the leading 0x, and will be 4 characters in length. For example, en-US will be returned 

as "0409" and en as "0009".

<div class="alert"><b>Note</b>  Use of MUI_LANGUAGE_NAME is recommended over MUI_LANGUAGE_ID.</div>
<div> </div>
<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetProcessPreferredUILanguages(
            System.UInt32 dwFlags,
            ref System.UInt32 pulNumLanguages,
            System.IntPtr pwszLanguagesBuffer,
            ref System.UInt32 pcchLanguagesBuffer
            );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>



<a href="https://msdn.microsoft.com/81f65561-886d-4c29-aca6-ea69bc865ea0">SetProcessPreferredUILanguages</a>
 

 

