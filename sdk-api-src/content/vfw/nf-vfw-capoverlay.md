---
UID: NF:vfw.capOverlay
title: capOverlay macro
author: windows-sdk-content
description: The capOverlay macro enables or disables overlay mode. In overlay mode, video is displayed using hardware overlay. You can use this macro or explicitly call the WM_CAP_SET_OVERLAY message.
old-location: multimedia\capoverlay.htm
tech.root: Multimedia
ms.assetid: a6508e33-7864-4f19-a844-0ba280028f43
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: "_win32_capOverlay, capOverlay, capOverlay macro [Windows Multimedia], multimedia.capoverlay, vfw/capOverlay"
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
 - capOverlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capOverlay macro


## -description



The <b>capOverlay</b> macro enables or disables overlay mode. In overlay mode, video is displayed using hardware overlay. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/b74c0619-2b70-46e0-9acd-43d658529233">WM_CAP_SET_OVERLAY</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param f

Overlay flag. Specify <b>TRUE</b> for this parameter to enable overlay mode or <b>FALSE</b> to disable it. 


## -remarks



Using an overlay does not require CPU resources.

The <b>fHasOverlay</b> member of the <b>CAPDRIVERCAPS</b> structure indicates whether the device is capable of overlay. The <b>fOverlayWindow</b> member of the <b>CAPSTATUS</b> structure indicates whether overlay mode is currently enabled.

Enabling overlay mode automatically disables preview mode.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

