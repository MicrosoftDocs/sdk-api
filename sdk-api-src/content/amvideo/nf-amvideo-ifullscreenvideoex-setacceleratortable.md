---
UID: NF:amvideo.IFullScreenVideoEx.SetAcceleratorTable
title: IFullScreenVideoEx::SetAcceleratorTable
author: windows-sdk-content
description: The SetAcceleratorTable method specifies an accelerator table that will be used to translate keyboard messages. The Full Screen Renderer filter does not support this method.
old-location: dshow\ifullscreenvideoex_setacceleratortable.htm
old-project: DirectShow
ms.assetid: aff393e8-e0a5-418d-8706-3fde96dbcfd9
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetAcceleratorTable method, IFullScreenVideoEx.SetAcceleratorTable, IFullScreenVideoEx::SetAcceleratorTable, IFullScreenVideoExSetAcceleratorTable, SetAcceleratorTable, SetAcceleratorTable method [DirectShow], SetAcceleratorTable method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetAcceleratorTable, dshow.ifullscreenvideoex_setacceleratortable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amvideo.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.SetAcceleratorTable
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFullScreenVideoEx::SetAcceleratorTable


## -description



The <code>SetAcceleratorTable</code> method specifies an accelerator table that will be used to translate keyboard messages. The Full Screen Renderer filter does not support this method.




## -parameters




### -param hwnd [in]

Handle of the window that will receive the translated messages.


### -param hAccel [in]

Handle to the accelerator table.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

