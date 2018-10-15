---
UID: NF:winnls.GetSystemDefaultUILanguage
title: GetSystemDefaultUILanguage function
author: windows-sdk-content
description: Retrieves the language identifier for the system default UI language of the operating system, also known as the &#0034;install language&#0034; on Windows Vista and later. For more information, see User Interface Language Management.
old-location: intl\getsystemdefaultuilanguage.htm
tech.root: Intl
ms.assetid: 34fc125d-0f0b-43d0-aa2b-91501bd6cd26
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetSystemDefaultUILanguage, GetSystemDefaultUILanguage function [Internationalization for Windows Applications], _win32_GetSystemDefaultUILanguage, intl.getsystemdefaultuilanguage, winnls/GetSystemDefaultUILanguage
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - GetSystemDefaultUILanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemDefaultUILanguage function


## -description


Retrieves the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> for the system default UI language of the operating system, also known as the "install language" on Windows Vista and later. For more information, see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a>.


## -parameters






## -returns



Returns the language identifier for the system default UI language of the operating system. For more information, see the Remarks section.




## -remarks



This function never returns a language identifier for a Language Interface Pack (LIP). It also never returns a language identifier corresponding to the locale identifier <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a> or <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>.

Note that this function does not necessarily return the identifier for the first language in the system preferred UI languages list. Therefore the return might not match the first element retrieved by <a href="https://msdn.microsoft.com/2948b495-c400-4227-94fb-7c4f5171ecae">GetSystemPreferredUILanguages</a>.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 GetSystemDefaultUILanguage();

```





## -see-also




<a href="https://msdn.microsoft.com/f97df853-fc40-4529-b8a5-27069863a9b9">EnumUILanguages</a>



<a href="https://msdn.microsoft.com/2948b495-c400-4227-94fb-7c4f5171ecae">GetSystemPreferredUILanguages</a>



<a href="https://msdn.microsoft.com/0de3a2d8-e595-4068-805c-b9bcba7ada91">GetUserDefaultUILanguage</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

