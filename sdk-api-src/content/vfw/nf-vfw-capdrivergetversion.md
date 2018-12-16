---
UID: NF:vfw.capDriverGetVersion
title: capDriverGetVersion macro
author: windows-sdk-content
description: The capDriverGetVersion macro returns the version information of the capture driver connected to a capture window. You can use this macro or explicitly send the WM_CAP_DRIVER_GET_VERSION message.
old-location: multimedia\capdrivergetversion.htm
tech.root: Multimedia
ms.assetid: 35afaef2-dc83-4b72-92e5-2fb9a75e90ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_capDriverGetVersion, capDriverGetVersion, capDriverGetVersion macro [Windows Multimedia], multimedia.capdrivergetversion, vfw/capDriverGetVersion"
ms.topic: macro
req.header: vfw.h
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
 - Vfw.h
api_name:
 - capDriverGetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capDriverGetVersion macro


## -description



The <b>capDriverGetVersion</b> macro returns the version information of the capture driver connected to a capture window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/762ebe7e-0d09-46ea-ab17-86061f0bd8f9">WM_CAP_DRIVER_GET_VERSION</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szVer

Pointer to an application-defined buffer used to return the version information as a null-terminated string. 


### -param wSize

Size, in bytes, of the application-defined buffer referenced by <i>szVer</i>. 


## -remarks



The version information is a text string retrieved from the driver's resource area. Applications should allocate approximately 40 bytes for this string. If version information is not available, a <b>NULL</b> string is returned.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

