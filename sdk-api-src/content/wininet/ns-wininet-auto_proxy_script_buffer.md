---
UID: NS:wininet.AUTO_PROXY_SCRIPT_BUFFER
title: AUTO_PROXY_SCRIPT_BUFFER
author: windows-sdk-content
description: The AUTO_PROXY_SCRIPT_BUFFER structure is used to pass an autoproxy script in a buffer to InternetInitializeAutoProxyDll , instead of identifying a file that InternetInitializeAutoProxyDll opens.
old-location: wininet\auto_proxy_script_buffer.htm
old-project: WinInet
ms.assetid: 4bbe875a-1eac-421a-90c6-ac60b2229b4c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPAUTO_PROXY_SCRIPT_BUFFER, AUTO_PROXY_SCRIPT_BUFFER, AUTO_PROXY_SCRIPT_BUFFER structure [WinINet], wininet.auto_proxy_script_buffer, wininet/AUTO_PROXY_SCRIPT_BUFFER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wininet.h
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
req.typenames: AUTO_PROXY_SCRIPT_BUFFER, *LPAUTO_PROXY_SCRIPT_BUFFER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - AUTO_PROXY_SCRIPT_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# AUTO_PROXY_SCRIPT_BUFFER structure


## -description


The <b>AUTO_PROXY_SCRIPT_BUFFER</b> structure is used to pass an autoproxy script in a buffer to <a href="https://msdn.microsoft.com/d55d64cb-ee92-4366-a1bb-f5d421ed81c8">InternetInitializeAutoProxyDll</a> , instead of identifying a file that <b>InternetInitializeAutoProxyDll</b> opens.


## -struct-fields




### -field dwStructSize

Size of this structure. Always set to "sizeof(AUTO_PROXY_SCRIPT_BUFFER)".


### -field lpszScriptBuffer

Pointer to the script buffer being passed using this structure.


### -field dwScriptBufferSize

Size of the script buffer pointed to by <b>lpszScriptBuffer</b>.


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d55d64cb-ee92-4366-a1bb-f5d421ed81c8">InternetInitializeAutoProxyDll</a>
 

 

