---
UID: NF:vfw.capPreviewScale
title: capPreviewScale macro
author: windows-sdk-content
description: The capPreviewScale macro enables or disables scaling of the preview video images.
old-location: multimedia\cappreviewscale.htm
tech.root: Multimedia
ms.assetid: 32f432a7-76be-4b75-8863-bc67cdcda781
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "_win32_capPreviewScale, capPreviewScale, capPreviewScale macro [Windows Multimedia], multimedia.cappreviewscale, vfw/capPreviewScale"
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
 - capPreviewScale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capPreviewScale macro


## -description



The <b>capPreviewScale</b> macro enables or disables scaling of the preview video images. If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/f15f1d18-2c5a-40c1-baa1-0d18549bee23">WM_CAP_SET_SCALE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param f

Preview scaling flag. Specify <b>TRUE</b> for this parameter to stretch preview frames to the size of the capture window or <b>FALSE</b> to display them at their natural size. 


## -remarks



Scaling preview images controls the immediate presentation of captured frames within the capture window. It has no effect on the size of the frames saved to file.

Scaling has no effect when using overlay to display video in the frame buffer.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

