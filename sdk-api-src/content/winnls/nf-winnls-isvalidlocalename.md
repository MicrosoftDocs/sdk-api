---
UID: NF:winnls.IsValidLocaleName
title: IsValidLocaleName function
author: windows-sdk-content
description: Determines if the specified locale name is valid for a locale that is installed or supported on the operating system.Note  An application running only on Windows Vista and later should call this function in preference to IsValidLocale to determine the validity of a supplemental locale.
old-location: intl\isvalidlocalename.htm
old-project: Intl
ms.assetid: cd1b5a4e-7a9c-47a1-9ece-284fce3d5be4
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: IsValidLocaleName, IsValidLocaleName function [Internationalization for Windows Applications], _win32_IsValidLocaleName, intl.isvalidlocalename, winnls/IsValidLocaleName
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
 - IsValidLocaleName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IsValidLocaleName function


## -description


Determines if the specified <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a> is valid for a locale that is installed or supported on the operating system.<div class="alert"><b>Note</b>  An application running only on Windows Vista and later should call this function in preference to <a href="https://msdn.microsoft.com/b0fb95ff-106d-4269-a696-d39f87fbd745">IsValidLocale</a> to determine the validity of a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">supplemental locale</a>.</div>
<div> </div>



## -parameters




### -param lpLocaleName [in]

Pointer to the locale name to validate.


## -returns



Returns a nonzero value if the locale name is valid, or returns 0 for an invalid name.




## -remarks



On Windows Vista and later, all supported locales should be installed on all operating systems.

This function can handle the name of a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locale</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.


#### Examples

An example showing the use of this function can be found in <a href="https://msdn.microsoft.com/0502dba0-a26f-4238-b68e-bb41ef17ff08">NLS: Name-based APIs Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>



<a href="https://msdn.microsoft.com/b0fb95ff-106d-4269-a696-d39f87fbd745">IsValidLocale</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

