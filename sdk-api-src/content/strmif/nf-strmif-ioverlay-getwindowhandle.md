---
UID: NF:strmif.IOverlay.GetWindowHandle
title: IOverlay::GetWindowHandle method
author: windows-driver-content
description: The GetWindowHandle method retrieves the current window handle.
old-location: dshow\ioverlay_getwindowhandle.htm
old-project: DirectShow
ms.assetid: f2d4cc53-ab0a-4c15-9818-3f312a13d4e1
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetWindowHandle method [DirectShow], GetWindowHandle method [DirectShow], IOverlay interface, GetWindowHandle,IOverlay.GetWindowHandle, IOverlay, IOverlay interface [DirectShow], GetWindowHandle method, IOverlay::GetWindowHandle, IOverlayGetWindowHandle, dshow.ioverlay_getwindowhandle, strmif/IOverlay::GetWindowHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IOverlay.GetWindowHandle
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IOverlay::GetWindowHandle method


## -description



The <code>GetWindowHandle</code> method retrieves the current window handle.




## -parameters




### -param pHwnd [out]

Receives the window handle.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 

