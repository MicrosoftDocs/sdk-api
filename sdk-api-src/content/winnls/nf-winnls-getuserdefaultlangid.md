---
UID: NF:winnls.GetUserDefaultLangID
title: GetUserDefaultLangID function
author: windows-sdk-content
description: Returns the language identifier of the Region Format setting for the current user.
old-location: intl\getuserdefaultlangid.htm
tech.root: Intl
ms.assetid: b1f25fc1-9435-4e9b-b8d0-a670a198ab3a
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetUserDefaultLangID, GetUserDefaultLangID function [Internationalization for Windows Applications], _win32_GetUserDefaultLangID, intl.getuserdefaultlangid, winnls/GetUserDefaultLangID
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GetUserDefaultLangID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetUserDefaultLangID function


## -description


Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the Region Format setting for the current user.


## -parameters






## -returns



Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> for the current user as set under <b>Control Panel</b> &gt; <b>Clock, Language, and Region</b> &gt; <b>Change date, time, or number formats</b> &gt; <b>Formats</b> tab &gt; <b>Format</b> dropdown.

For more information on language identifiers, see <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.




## -remarks



The return value is not necessarily the same as that returned by <a href="https://msdn.microsoft.com/cf9d2f64-a8ad-46f8-9e91-a927b6b3ce08">GetSystemDefaultLangID</a>, even for a single-user computer.




## -see-also




<a href="https://msdn.microsoft.com/cf9d2f64-a8ad-46f8-9e91-a927b6b3ce08">GetSystemDefaultLangID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

