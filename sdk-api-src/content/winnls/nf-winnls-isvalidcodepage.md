---
UID: NF:winnls.IsValidCodePage
title: IsValidCodePage function
author: windows-sdk-content
description: Determines if a specified code page is valid.
old-location: intl\isvalidcodepage.htm
tech.root: Intl
ms.assetid: 7bd16f61-a534-4ada-ae27-d5deb47870a9
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IsValidCodePage, IsValidCodePage function [Internationalization for Windows Applications], _win32_IsValidCodePage, intl.isvalidcodepage, winnls/IsValidCodePage
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
 - IsValidCodePage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsValidCodePage function


## -description


Determines if a specified code page is valid.


## -parameters




### -param CodePage [in]


<a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code page identifier</a> for the code page to check.


## -returns



Returns a nonzero value if the code page is valid, or 0 if the code page is invalid.




## -remarks



A code page is considered valid only if it is installed on the operating system. Unicode is preferred.

Starting with Windows Vista, all code pages that can be installed are loaded by default.




## -see-also




<a href="https://msdn.microsoft.com/a28c3f08-ee76-4e3f-b14d-fabc0af98fef">GetACP</a>



<a href="https://msdn.microsoft.com/f7401cd5-d0ed-49b1-b8fc-dda8df99e6b6">GetCPInfo</a>



<a href="https://msdn.microsoft.com/e6d42641-4bbe-44d8-baea-1087e48dae7d">GetOEMCP</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

