---
UID: NF:winnls.SetProcessPreferredUILanguages
title: SetProcessPreferredUILanguages function
author: windows-sdk-content
description: Sets the process preferred UI languages for the application process. For more information, see User Interface Language Management.
old-location: intl\setprocesspreferreduilanguages.htm
tech.root: Intl
ms.assetid: 81f65561-886d-4c29-aca6-ea69bc865ea0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, SetProcessPreferredUILanguages, SetProcessPreferredUILanguages function [Internationalization for Windows Applications], intl.setprocesspreferreduilanguages, winnls/SetProcessPreferredUILanguages
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - SetProcessPreferredUILanguages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetProcessPreferredUILanguages function


## -description


Sets the process preferred UI languages for the application process. For more information, see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a>.


## -parameters




### -param dwFlags [in]

Flags identifying the language format to use for the process preferred UI languages. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME. 

We recommend that you use MUI_LANGUAGE_NAME instead of MUI_LANGUAGE_ID.

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
The input parameter language strings are in <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The input parameter language strings are in <a href="https://msdn.microsoft.com/e8c54168-22b3-435e-b19a-9b34adcdb018">language name</a> format.

</td>
</tr>
</table>
 


### -param pwszLanguagesBuffer [in, optional]

Pointer to a double null-terminated multi-string buffer that contains an ordered, null-delimited list in decreasing order of preference. If there are more than five languages in the buffer, the function only sets the first five valid languages.

Alternatively, this parameter can contain <b>NULL</b> if no language list is required. In this case, the function clears the preferred UI languages for the process.


### -param pulNumLanguages [out, optional]

Pointer to the number of languages that has been set in the process language list from the input buffer, up to a maximum of five.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return the following error code:

<ul>
<li>ERROR_INVALID_PARAMETER. An invalid parameter is specified.</li>
</ul>
If the process preferred UI languages list is empty or if the languages specified for the process are not valid, the function succeeds and sets 0 in the <i>pulNumLanguages</i> parameter.





## -remarks



Ideally, applications will call <b>SetProcessPreferredUILanguages</b> as soon as possible after launching.

After this function returns, the application can call <a href="https://msdn.microsoft.com/115fd1f4-39ae-4c69-aa42-606617a989aa">GetProcessPreferredUILanguages</a> to verify and examine the resulting language list.

When MUI_LANGUAGE_ID is specified, the input parameter language strings must use hexadecimal language 

identifiers that do not include the leading 0x, and are 4 characters in length. For example, en-US should be 

passed as "0409" and en as "0009".

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
        static extern System.Boolean SetProcessPreferredUILanguages(
            System.UInt32 dwFlags,
            System.String pwszLanguagesBuffer,
            ref System.UInt32 pulNumLanguages
            );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/115fd1f4-39ae-4c69-aa42-606617a989aa">GetProcessPreferredUILanguages</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

