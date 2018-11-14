---
UID: NF:winnls.GetSystemDefaultLangID
title: GetSystemDefaultLangID function
author: windows-sdk-content
description: Returns the language identifier for the system locale.
old-location: intl\getsystemdefaultlangid.htm
tech.root: Intl
ms.assetid: cf9d2f64-a8ad-46f8-9e91-a927b6b3ce08
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetSystemDefaultLangID, GetSystemDefaultLangID function [Internationalization for Windows Applications], _win32_GetSystemDefaultLangID, intl.getsystemdefaultlangid, winnls/GetSystemDefaultLangID
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
 - GetSystemDefaultLangID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetSystemDefaultLangID
: 
---

# GetSystemDefaultLangID function


## -description


Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> for the system locale.


## -parameters






## -returns



Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> for the system locale. This is  the language used when displaying text in programs that do not support Unicode. It is set by the Administrator under <b>Control Panel</b> &gt; <b>Clock, Language, and Region</b> &gt; <b>Change date, time, or number formats</b> &gt; <b>Administrative</b> tab.

For more information on language identifiers, see <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a>



<a href="https://msdn.microsoft.com/b1f25fc1-9435-4e9b-b8d0-a670a198ab3a">GetUserDefaultLangID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

