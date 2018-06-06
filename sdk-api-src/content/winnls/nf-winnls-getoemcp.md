---
UID: NF:winnls.GetOEMCP
title: GetOEMCP function
author: windows-sdk-content
description: Returns the current original equipment manufacturer (OEM) code page identifier for the operating system.
old-location: intl\getoemcp.htm
old-project: Intl
ms.assetid: e6d42641-4bbe-44d8-baea-1087e48dae7d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetOEMCP, GetOEMCP function [Internationalization for Windows Applications], _win32_GetOEMCP, intl.getoemcp, winnls/GetOEMCP
ms.prod: windows
ms.technology: windows-sdk
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
 - GetOEMCP
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetOEMCP function


## -description


Returns the current original equipment manufacturer (OEM) code page identifier for the operating system.
<div class="alert"><b>Note</b>   The ANSI code pages can be different on different computers, or can be changed for a single computer, leading to data corruption. For the most consistent results, applications should use Unicode, such as UTF-8 or UTF-16, instead of a specific code page.</div><div> </div>

## -parameters






## -returns



Returns the current OEM code page identifier for the operating system.




## -remarks



See <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a> for a list of OEM and other code pages.




## -see-also




<a href="https://msdn.microsoft.com/a28c3f08-ee76-4e3f-b14d-fabc0af98fef">GetACP</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

