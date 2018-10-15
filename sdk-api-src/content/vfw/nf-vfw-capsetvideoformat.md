---
UID: NF:vfw.capSetVideoFormat
title: capSetVideoFormat macro
author: windows-sdk-content
description: The capSetVideoFormat macro sets the format of captured video data. You can use this macro or explicitly call the WM_CAP_SET_VIDEOFORMAT message.
old-location: multimedia\capsetvideoformat.htm
tech.root: Multimedia
ms.assetid: 3c4bee26-d578-463b-8d97-6cdc78957ce0
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "_win32_capSetVideoFormat, capSetVideoFormat, capSetVideoFormat macro [Windows Multimedia], multimedia.capsetvideoformat, vfw/capSetVideoFormat"
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
 - capSetVideoFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capSetVideoFormat macro


## -description



The <b>capSetVideoFormat</b> macro sets the format of captured video data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4f9cf90d-7ccb-4fc7-aad5-3d7e082526be">WM_CAP_SET_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure. 


### -param wSize

The size, in bytes, of the structure referenced by <i>psVideoFormat</i>. 


## -remarks



Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

