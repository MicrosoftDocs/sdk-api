---
UID: NF:vfw.capCaptureGetSetup
title: capCaptureGetSetup macro
author: windows-sdk-content
description: The capCaptureGetSetup macro retrieves the current settings of the streaming capture parameters. You can use this macro or explictly send the WM_CAP_GET_SEQUENCE_SETUP message.
old-location: multimedia\capcapturegetsetup.htm
tech.root: Multimedia
ms.assetid: 198b1aae-b719-4fb8-a11d-859eaf7a4606
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "_win32_capCaptureGetSetup, capCaptureGetSetup, capCaptureGetSetup macro [Windows Multimedia], multimedia.capcapturegetsetup, vfw/capCaptureGetSetup"
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
 - capCaptureGetSetup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capCaptureGetSetup macro


## -description



The <b>capCaptureGetSetup</b> macro retrieves the current settings of the streaming capture parameters. You can use this macro or explictly send the <a href="https://msdn.microsoft.com/2220c92a-1994-4f15-9730-1cf01972dda6">WM_CAP_GET_SEQUENCE_SETUP</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure. 


### -param wSize

Size, in bytes, of the structure referenced by s. 


## -remarks



For information about the parameters used to control streaming capture, see the <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

