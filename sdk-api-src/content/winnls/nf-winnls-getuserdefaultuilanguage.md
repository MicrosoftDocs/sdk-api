---
UID: NF:winnls.GetUserDefaultUILanguage
title: GetUserDefaultUILanguage function
author: windows-sdk-content
description: Returns the language identifier for the user UI language for the current user.
old-location: intl\getuserdefaultuilanguage.htm
old-project: Intl
ms.assetid: 0de3a2d8-e595-4068-805c-b9bcba7ada91
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetUserDefaultUILanguage, GetUserDefaultUILanguage function [Internationalization for Windows Applications], _win32_GetUserDefaultUILanguage, intl.getuserdefaultuilanguage, winnls/GetUserDefaultUILanguage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - kernel32.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - GetUserDefaultUILanguage
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetUserDefaultUILanguage function


## -description


Returns the language identifier for the user UI language for the current user. If the current user has not set a language, <b>GetUserDefaultUILanguage</b> returns the preferred language set for the system. If there is no preferred language set for the system, then the system default UI language (also known as "install language") is returned. For more information about the user UI language, see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a>.


## -parameters






## -returns



Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> for the user UI language for the current user.




## -remarks



This function returns only a language identifier. An application can retrieve the language name using the <a href="https://msdn.microsoft.com/0800642c-c133-4993-bd16-6bdbf7518f1c">GetUserPreferredUILanguages</a> function.

If the user UI language is part of a Language Interface Pack (LIP) and corresponds to a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">supplemental locale</a>, this function returns <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>.

<b>Windows Me, Windows 2000, Windows XP, Windows Server 2003:</b> The <b>GetUserDefaultUILanguage</b> function retrieves the language identifier for the current user language. If MUI is not installed on the operating system, the function retrieves the default computer user interface language.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 GetUserDefaultUILanguage();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f97df853-fc40-4529-b8a5-27069863a9b9">EnumUILanguages</a>



<a href="https://msdn.microsoft.com/34fc125d-0f0b-43d0-aa2b-91501bd6cd26">GetSystemDefaultUILanguage</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

