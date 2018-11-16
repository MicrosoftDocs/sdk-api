---
UID: NF:vfw.capCaptureSetSetup
title: capCaptureSetSetup macro
author: windows-sdk-content
description: The capCaptureSetSetup macro sets the configuration parameters used with streaming capture. You can use this macro or explicitly send the WM_CAP_SET_SEQUENCE_SETUP message.
old-location: multimedia\capcapturesetsetup.htm
tech.root: Multimedia
ms.assetid: 663dcb34-6b11-4208-b5d6-216799fb774d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_win32_capCaptureSetSetup, capCaptureSetSetup, capCaptureSetSetup macro [Windows Multimedia], multimedia.capcapturesetsetup, vfw/capCaptureSetSetup"
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
 - capCaptureSetSetup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- vfw.h
: 
- capCaptureSetSetup
: 
---

# capCaptureSetSetup macro


## -description



The <b>capCaptureSetSetup</b> macro sets the configuration parameters used with streaming capture. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/ba9adb26-6627-469b-a836-f4f277ddb7c4">WM_CAP_SET_SEQUENCE_SETUP</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a CAPTUREPARMS structure. 


### -param wSize

Size, in bytes, of the structure referenced by s. 


## -remarks



For information about the parameters used to control streaming capture, see the <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

