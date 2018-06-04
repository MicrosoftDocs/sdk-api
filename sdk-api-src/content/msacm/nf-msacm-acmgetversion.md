---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

