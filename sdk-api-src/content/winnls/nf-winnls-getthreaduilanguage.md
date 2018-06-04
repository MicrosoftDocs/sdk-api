---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetThreadUILanguage function


## -description


Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the first user interface language for the current thread.


## -parameters






## -returns



Returns the identifier for a language explicitly associated with the thread by <a href="https://msdn.microsoft.com/30a0cecf-0ed1-4c03-bd5e-da07b1828c75">SetThreadUILanguage</a> or <a href="https://msdn.microsoft.com/32a8117c-2cb2-4559-8e86-9fad5b28aa5b">SetThreadPreferredUILanguages</a>. Alternatively, if no language has been explicitly associated with the current thread, the identifier can indicate a user or system user interface language.




## -remarks



Calling this function is identical to calling <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> with <i>dwFlags</i> set to MUI_MERGE_SYSTEM_FALLBACK | MUI_MERGE_USER_FALLBACK | MUI_LANGUAGE_ID and using the first language in the retrieved list.

The return value for this function does not provide useful information about a Language Interface Pack (LIP) language if that language corresponds to a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">supplemental locale</a>. For such a language, the function returns the hexadecimal value "1400", which corresponds to <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a> if that language is specified in the user preferred UI languages list. If the language is not specified in the user preferred UI languages list, the function returns the value "1000", corresponding to <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 GetThreadUILanguage();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>



<a href="https://msdn.microsoft.com/32a8117c-2cb2-4559-8e86-9fad5b28aa5b">SetThreadPreferredUILanguages</a>



<a href="https://msdn.microsoft.com/30a0cecf-0ed1-4c03-bd5e-da07b1828c75">SetThreadUILanguage</a>
 

 

