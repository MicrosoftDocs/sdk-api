---
UID: NF:winnls.SetThreadLocale
title: SetThreadLocale function
author: windows-sdk-content
description: Sets the current locale of the calling thread.
old-location: intl\setthreadlocale.htm
tech.root: Intl
ms.assetid: d86193c7-9b3a-422b-b76c-ff1992f68958
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetThreadLocale, SetThreadLocale function [Internationalization for Windows Applications], _win32_SetThreadLocale, intl.setthreadlocale, winnls/SetThreadLocale
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - SetThreadLocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadLocale function


## -description


Sets the current locale of the calling thread.


## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

## -returns



The function should return an LCID on success. This is the LCID of the previous thread locale.




## -remarks



When a thread is created, it uses the user locale. This value is returned by <a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>. The user locale can be modified for future processes and thread creation using the regional and language options portion of the Control Panel. The thread locale can also be changed using <b>SetThreadLocale</b>.

<b>SetThreadLocale</b> affects the selection of resources with a <a href="https://msdn.microsoft.com/175e27e2-903a-4aaf-89ef-532166b167e8">LANGUAGE</a> statement. The statement affects such functions as <a href="_win32_createdialog_cpp">CreateDialog</a>, <a href="_win32_dialogbox_cpp">DialogBox</a>, <a href="_win32_loadmenu_cpp">LoadMenu</a>, <a href="_win32_loadstring_cpp">LoadString</a>, and <a href="_win32_findresource_cpp">FindResource</a>. It sets the code page implied by CP_THREAD_ACP, but does not affect <a href="_win32_findresourceex_cpp">FindResourceEx</a>. For more information, see <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a>.

<b>Windows Vista and later: </b> Do not use <b>SetThreadLocale</b> to select a user interface language. The resource loader selects the resource that is defined in the .rc file with a <a href="https://msdn.microsoft.com/175e27e2-903a-4aaf-89ef-532166b167e8">LANGUAGE</a> statement, or the application can use <a href="_win32_findresourceex_cpp">FindResourceEx</a>. Additionally, the application can use <a href="https://msdn.microsoft.com/30a0cecf-0ed1-4c03-bd5e-da07b1828c75">SetThreadUILanguage</a>.
      

<b>Windows 2000, Windows XP:</b> Do not use <b>SetThreadLocale</b> to select a user interface language. To select the resource that is defined in the .rc file with a <a href="https://msdn.microsoft.com/175e27e2-903a-4aaf-89ef-532166b167e8">LANGUAGE</a> statement, the application must use the <a href="_win32_findresourceex_cpp">FindResourceEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a>



<a href="https://msdn.microsoft.com/4d77f78b-f059-40f3-b4ed-c3ffd09d9e9f">GetThreadLocale</a>



<a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

