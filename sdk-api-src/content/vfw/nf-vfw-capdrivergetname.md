---
UID: NF:vfw.capDriverGetName
title: capDriverGetName macro
author: windows-sdk-content
description: The capDriverGetName macro returns the name of the capture driver connected to the capture window. You can use this macro or explicitly call the WM_CAP_DRIVER_GET_NAME message.
old-location: multimedia\capdrivergetname.htm
old-project: Multimedia
ms.assetid: 50a5563d-5872-4cfd-a600-be83beceb0fe
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_win32_capDriverGetName, capDriverGetName, capDriverGetName macro [Windows Multimedia], multimedia.capdrivergetname, vfw/capDriverGetName"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	capDriverGetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capDriverGetName macro


## -description



The <b>capDriverGetName</b> macro returns the name of the capture driver connected to the capture window. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea">WM_CAP_DRIVER_GET_NAME</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to an application-defined buffer used to return the device name as a null-terminated string. 


### -param wSize

Size, in bytes, of the buffer referenced by <i>szName</i>. 


## -remarks



The name is a text string retrieved from the driver's resource area. Applications should allocate approximately 80 bytes for this string. If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

