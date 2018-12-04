---
UID: NF:amvideo.IFullScreenVideoEx.GetAcceleratorTable
title: IFullScreenVideoEx::GetAcceleratorTable
author: windows-sdk-content
description: The GetAcceleratorTable method retrieves the accelerator table currently being used to translate keyboard messages. The Full Screen Renderer filter does not support this method.
old-location: dshow\ifullscreenvideoex_getacceleratortable.htm
tech.root: DirectShow
ms.assetid: 60d1246b-8719-4f41-9088-2672f51dd6a9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetAcceleratorTable, GetAcceleratorTable method [DirectShow], GetAcceleratorTable method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetAcceleratorTable method, IFullScreenVideoEx.GetAcceleratorTable, IFullScreenVideoEx::GetAcceleratorTable, IFullScreenVideoExGetAcceleratorTable, amvideo/IFullScreenVideoEx::GetAcceleratorTable, dshow.ifullscreenvideoex_getacceleratortable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amvideo.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.GetAcceleratorTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFullScreenVideoEx::GetAcceleratorTable


## -description



The <code>GetAcceleratorTable</code> method retrieves the accelerator table currently being used to translate keyboard messages. The Full Screen Renderer filter does not support this method.




## -parameters




### -param phwnd [out]

Pointer to a variable that receives a window handle. The window receives translated messages.


### -param phAccel [out]

Pointer to a variable that receives a handle to the accelerator table.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

