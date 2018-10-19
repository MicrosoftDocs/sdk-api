---
UID: NF:vfw.capDriverGetCaps
title: capDriverGetCaps macro
author: windows-sdk-content
description: The capDriverGetCaps macro returns the hardware capabilities of the capture driver currently connected to a capture window. You can use this macro or explicitly send the WM_CAP_DRIVER_GET_CAPS message.
old-location: multimedia\capdrivergetcaps.htm
tech.root: Multimedia
ms.assetid: 2ca3a1b1-1d88-480f-b079-82da111c4565
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "_win32_capDriverGetCaps, capDriverGetCaps, capDriverGetCaps macro [Windows Multimedia], multimedia.capdrivergetcaps, vfw/capDriverGetCaps"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - capDriverGetCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capDriverGetCaps macro


## -description



The <b>capDriverGetCaps</b> macro returns the hardware capabilities of the capture driver currently connected to a capture window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/898a800c-1109-47cd-bcc9-cb61d86a4a2e">WM_CAP_DRIVER_GET_CAPS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to the <a href="https://msdn.microsoft.com/6d341be9-6b10-495b-803b-059ead1114cc">CAPDRIVERCAPS</a> structure to contain the hardware capabilities. 


### -param wSize

Size, in bytes, of the structure referenced by <i>psCaps</i>. 


## -remarks



The capabilities returned in <a href="https://msdn.microsoft.com/6d341be9-6b10-495b-803b-059ead1114cc">CAPDRIVERCAPS</a> are constant for a given capture driver. Applications need to retrieve this information once when the capture driver is first connected to a capture window.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

