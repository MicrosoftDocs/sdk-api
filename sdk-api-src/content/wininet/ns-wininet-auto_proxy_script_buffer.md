---
UID: NS:wininet.__unnamed_struct_39
title: AUTO_PROXY_SCRIPT_BUFFER (wininet.h)
author: windows-sdk-content
description: The AUTO_PROXY_SCRIPT_BUFFER structure is used to pass an autoproxy script in a buffer to InternetInitializeAutoProxyDll , instead of identifying a file that InternetInitializeAutoProxyDll opens.
old-location: wininet\auto_proxy_script_buffer.htm
tech.root: wininet
ms.assetid: 4bbe875a-1eac-421a-90c6-ac60b2229b4c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPAUTO_PROXY_SCRIPT_BUFFER, AUTO_PROXY_SCRIPT_BUFFER, AUTO_PROXY_SCRIPT_BUFFER structure [WinINet], wininet.auto_proxy_script_buffer, wininet/AUTO_PROXY_SCRIPT_BUFFER"
ms.topic: struct
f1_keywords: ["wininet/AUTO_PROXY_SCRIPT_BUFFER"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: AUTO_PROXY_SCRIPT_BUFFER, *LPAUTO_PROXY_SCRIPT_BUFFER
req.redist: 
ms.custom: 19H1
---

# AUTO_PROXY_SCRIPT_BUFFER structure


## -description


The <b>AUTO_PROXY_SCRIPT_BUFFER</b> structure is used to pass an autoproxy script in a buffer to <a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a> , instead of identifying a file that <b>InternetInitializeAutoProxyDll</b> opens.


## -struct-fields




### -field dwStructSize

Size of this structure. Always set to "sizeof(AUTO_PROXY_SCRIPT_BUFFER)".


### -field lpszScriptBuffer

Pointer to the script buffer being passed using this structure.


### -field dwScriptBufferSize

Size of the script buffer pointed to by <b>lpszScriptBuffer</b>.


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a>
 

 

