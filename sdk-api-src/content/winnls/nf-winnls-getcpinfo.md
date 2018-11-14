---
UID: NF:winnls.GetCPInfo
title: GetCPInfo function
author: windows-sdk-content
description: Retrieves information about any valid installed or available code page.
old-location: intl\getcpinfo.htm
tech.root: Intl
ms.assetid: f7401cd5-d0ed-49b1-b8fc-dda8df99e6b6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetCPInfo, GetCPInfo function [Internationalization for Windows Applications], _win32_GetCPInfo, intl.getcpinfo, winnls/GetCPInfo
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
 - GetCPInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetCPInfo
: 
---

# GetCPInfo function


## -description


Retrieves information about any valid installed or available code page. 
<div class="alert"><b>Note</b>  To obtain additional information about valid installed or available code pages, the application should use <a href="https://msdn.microsoft.com/c21ed6fe-85b6-438a-8f53-e30833e0c88a">GetCPInfoEx</a>.</div><div> </div>

## -parameters




### -param CodePage [in]

Identifier for the code page for which to retrieve information. For details, see the <i>CodePage</i> parameter of <a href="https://msdn.microsoft.com/c21ed6fe-85b6-438a-8f53-e30833e0c88a">GetCPInfoEx</a>.


### -param lpCPInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/accb7ce8-c1d0-4f89-9390-be26d7014de7">CPINFO</a> structure that receives information about the code page. See the Remarks section.


## -returns



Returns 1 if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:
				

<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



See Remarks for <a href="https://msdn.microsoft.com/c21ed6fe-85b6-438a-8f53-e30833e0c88a">GetCPInfoEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/accb7ce8-c1d0-4f89-9390-be26d7014de7">CPINFO</a>



<a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a>



<a href="https://msdn.microsoft.com/a28c3f08-ee76-4e3f-b14d-fabc0af98fef">GetACP</a>



<a href="https://msdn.microsoft.com/c21ed6fe-85b6-438a-8f53-e30833e0c88a">GetCPInfoEx</a>



<a href="https://msdn.microsoft.com/e6d42641-4bbe-44d8-baea-1087e48dae7d">GetOEMCP</a>



<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a>
 

 

