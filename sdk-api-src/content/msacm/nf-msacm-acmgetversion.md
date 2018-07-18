---
UID: NF:msacm.acmGetVersion
title: acmGetVersion function
author: windows-sdk-content
description: The acmGetVersion function returns the version number of the ACM.
old-location: multimedia\acmgetversion.htm
old-project: Multimedia
ms.assetid: 5a710149-0c3a-4dde-8069-db2e42826080
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "_win32_acmGetVersion, acmGetVersion, acmGetVersion function [Windows Multimedia], msacm/acmGetVersion, multimedia.acmgetversion"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msacm.h
req.include-header: 
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
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmGetVersion
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmGetVersion function


## -description



The <b>acmGetVersion</b> function returns the version number of the ACM.




## -parameters






## -returns



The version number is returned as a hexadecimal number of the form 0xAABBCCCC, where AA is the major version number, BB is the minor version number, and CCCC is the build number.




## -remarks



Win32 applications must verify that the ACM version is at least 0x03320000 (version 3.50) or greater before attempting to use any other ACM functions. The build number (CCCC) is always zero for the retail (non-debug) version of the ACM.

To display the ACM version for a user, an application should use the following format (note that the values should be printed as unsigned decimals):

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
{ 
    DWORD   dw; 
    TCHAR   ach[10]; 
 
    dw = acmGetVersion(); 
    _stprintf_s(ach, TEXT("%u.%.02u"), 
        HIWORD(dw) &gt;&gt; 8, HIWORD(dw) &amp; 0x00FF); 
} 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

