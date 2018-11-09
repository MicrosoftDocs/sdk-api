---
UID: NF:winhttp.WinHttpCheckPlatform
title: WinHttpCheckPlatform function
author: windows-sdk-content
description: The WinHttpCheckPlatform function determines whether the current platform is supported by this version of Microsoft Windows HTTP Services (WinHTTP).
old-location: http\winhttpcheckplatform.htm
tech.root: WinHttp
ms.assetid: 0daec97f-c1c9-4d87-8e24-485e262d8a85
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WinHttpCheckPlatform, WinHttpCheckPlatform function [WinHTTP], http.winhttpcheckplatform, winhttp.winhttpcheckplatform_function, winhttp/WinHttpCheckPlatform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpCheckPlatform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinHttpCheckPlatform function


## -description


The <b>WinHttpCheckPlatform</b> function determines whether the current platform is supported by this version of Microsoft Windows HTTP Services (WinHTTP).


## -parameters






## -returns



The return value is <b>TRUE</b> if the platform is supported by Microsoft Windows HTTP Services (WinHTTP), or <b>FALSE</b> otherwise.




## -remarks



This function is useful if your application uses Microsoft Windows HTTP Services (WinHTTP), but also supports platforms that WinHTTP does not.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

 WinHTTP version 5.1 is  an operating-system component of Windows 2000 with Service Pack 3 (SP3) and later (except Datacenter Server), Windows XP with Service Pack 1 (SP1) and later, and Windows Server 2003. In Windows Server 2003, WinHTTP is a system side-by-side assembly.

For more information, see <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a>.


#### Examples

The following example shows how to determine whether the current platform is supported.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    if (WinHttpCheckPlatform( ))
        printf("This platform is supported by WinHTTP.\n");
    else
        printf("This platform is NOT supported by WinHTTP.\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>
 

 

