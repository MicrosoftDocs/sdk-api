---
UID: NF:winnls.GetCPInfoExA
title: GetCPInfoExA function
author: windows-sdk-content
description: Retrieves information about any valid installed or available code page.
old-location: intl\getcpinfoex.htm
old-project: Intl
ms.assetid: c21ed6fe-85b6-438a-8f53-e30833e0c88a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CP_THREAD_ACP, GetCPInfoEx, GetCPInfoEx function [Internationalization for Windows Applications], GetCPInfoExA, GetCPInfoExW, _win32_GetCPInfoEx, intl.getcpinfoex, winnls/GetCPInfoEx, winnls/GetCPInfoExA, winnls/GetCPInfoExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCPInfoExW (Unicode) and GetCPInfoExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Localization-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-l1-2-0.dll
-	API-MS-Win-Core-Localization-l1-2-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-L1-2-2.dll
-	API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	GetCPInfoEx
-	GetCPInfoExA
-	GetCPInfoExW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCPInfoExA function


## -description


Retrieves information about any valid installed or available code page.


## -parameters




### -param CodePage [in]

Identifier for the code page for which to retrieve information. The application can specify the code page identifier for any installed or available code page, or one of the following predefined values. See <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a> for a list of identifiers for ANSI and other code pages.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CP_ACP"></a><a id="cp_acp"></a><dl>
<dt><b>CP_ACP</b></dt>
</dl>
</td>
<td width="60%">
Use the system default Windows ANSI code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_MACCP"></a><a id="cp_maccp"></a><dl>
<dt><b>CP_MACCP</b></dt>
</dl>
</td>
<td width="60%">
Use the system default Macintosh code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_OEMCP"></a><a id="cp_oemcp"></a><dl>
<dt><b>CP_OEMCP</b></dt>
</dl>
</td>
<td width="60%">
Use the system default OEM code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_THREAD_ACP"></a><a id="cp_thread_acp"></a><dl>
<dt><b>CP_THREAD_ACP</b></dt>
</dl>
</td>
<td width="60%">

                Use the current thread's ANSI code page.

</td>
</tr>
</table>
 


### -param dwFlags [in]

Reserved; must be 0.


### -param lpCPInfoEx [out]

Pointer to a <a href="https://msdn.microsoft.com/9639bb11-477e-45ee-b9fb-d5d099925e00">CPINFOEX</a> structure that receives information about the code page.


## -returns




            Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:


<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



The information retrieved in the <a href="https://msdn.microsoft.com/9639bb11-477e-45ee-b9fb-d5d099925e00">CPINFOEX</a> structure is not always useful for all code pages. To determine buffer sizes, for example, the application should call <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> or <a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a> to request an accurate buffer size. If <b>CPINFOEX</b> settings indicate that a lead byte exists, the conversion function does not necessarily handle lead bytes differently, for example, in the case of a missing or illegal trail byte.




## -see-also




<a href="https://msdn.microsoft.com/9639bb11-477e-45ee-b9fb-d5d099925e00">CPINFOEX</a>



<a href="https://msdn.microsoft.com/a28c3f08-ee76-4e3f-b14d-fabc0af98fef">GetACP</a>



<a href="https://msdn.microsoft.com/f7401cd5-d0ed-49b1-b8fc-dda8df99e6b6">GetCPInfo</a>



<a href="https://msdn.microsoft.com/e6d42641-4bbe-44d8-baea-1087e48dae7d">GetOEMCP</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

