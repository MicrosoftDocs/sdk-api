---
UID: NF:winnls.SetThreadUILanguage
title: SetThreadUILanguage function
author: windows-sdk-content
description: Sets the user interface language for the current thread.
old-location: intl\setthreaduilanguage.htm
old-project: Intl
ms.assetid: 30a0cecf-0ed1-4c03-bd5e-da07b1828c75
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: SetThreadUILanguage, SetThreadUILanguage function [Internationalization for Windows Applications], _win32_SetThreadUILanguage, intl.setthreaduilanguage, winnls/SetThreadUILanguage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - SetThreadUILanguage
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetThreadUILanguage function


## -description


Sets the user interface language for the current thread.

<b>Windows Vista and later:</b> This function cannot clear the thread preferred UI languages list. Your MUI application should call <a href="https://msdn.microsoft.com/32a8117c-2cb2-4559-8e86-9fad5b28aa5b">SetThreadPreferredUILanguages</a> to clear the language list.

<b>Windows XP:</b> This function is limited to allowing the operating system to identify and set a value that is safe to use on the Windows console.


## -parameters




### -param LangId [in]


<a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language identifier</a> for the user interface language for the thread.

<b>Windows Vista and later:</b> The application can specify a language identifier of 0 or a nonzero identifier. For more information, see the Remarks section.

<b>Windows XP:</b> The application can only set this parameter to 0. This setting causes the function to select the language that best supports the console display. For more information, see the Remarks section.


## -returns



Returns the input language identifier if successful. If the input identifier is nonzero, the function returns that value. If the language identifier is 0, the function always succeeds and returns the identifier of the language that best supports the Windows console. See the Remarks section.

If the input language identifier is nonzero and the function fails, the return value differs from the input language identifier. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When a thread is created, the thread user interface language setting is empty and the user interface for the thread is displayed in the user-selected language. This function enables the application to change the user interface language for the current running thread.

<b>Windows Vista and later:</b> Calling this function and specifying 0 for the language identifier is identical to calling <a href="https://msdn.microsoft.com/32a8117c-2cb2-4559-8e86-9fad5b28aa5b">SetThreadPreferredUILanguages</a> with the MUI_CONSOLE_FILTER flag set. If the application specifies a valid nonzero language identifier, the function sets a particular user interface language for the thread. After specifying 0 for the language identifier, the application cannot use any of the following constants to correspond to a language identifier:


<ul>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
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
<b>Windows XP:</b> When the application calls this function with a language identifier of 0, the function first verifies that the current user interface does not require Uniscribe, and that it is supported by the console <a href="https://msdn.microsoft.com/866f09f4-629e-4097-a974-fbda9389d077">code page</a>. If the user interface passes these tests, the function uses the supplied value. If not, the function changes the thread user interface language to a language that the Windows console can display. Windows XP does not support a concept of thread user interface language separate from thread locale. Therefore, this function changes the thread locale on Windows XP. It is easy for your application to set a thread to use the most appropriate language for console display, based on user and system preferred UI languages, the language for non-Unicode applications, and the capabilities of the console.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 SetThreadUILanguage(
            System.UInt16 LangId
            );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c10cbf84-8aaf-46c7-8b2f-e719e30f2556">GetThreadUILanguage</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>



<a href="https://msdn.microsoft.com/32a8117c-2cb2-4559-8e86-9fad5b28aa5b">SetThreadPreferredUILanguages</a>
 

 

