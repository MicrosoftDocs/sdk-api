---
UID: NF:vfw.capSetScrollPos
title: capSetScrollPos macro
author: windows-driver-content
description: The capSetScrollPos macro defines the portion of the video frame to display in the capture window.
old-location: multimedia\capsetscrollpos.htm
old-project: Multimedia
ms.assetid: a5af0d75-ae9f-41f2-90cb-8ede7c2f454a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "_win32_capSetScrollPos, capSetScrollPos, capSetScrollPos macro [Windows Multimedia], multimedia.capsetscrollpos, vfw/capSetScrollPos"
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	capSetScrollPos
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capSetScrollPos macro


## -description



The <b>capSetScrollPos</b> macro defines the portion of the video frame to display in the capture window. This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/545605e4-6b1f-403a-a3ab-0fd6750ae776">WM_CAP_SET_SCROLL</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param lpP

Address to contain the desired scroll position. 


## -remarks



The scroll position affects the image in both preview and overlay modes.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

