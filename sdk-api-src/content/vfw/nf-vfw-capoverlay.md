---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

