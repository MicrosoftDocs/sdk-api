---
UID: NF:strmif.IOverlayNotify2.OnDisplayChange
title: IOverlayNotify2::OnDisplayChange
author: windows-sdk-content
description: The OnDisplayChange method provides notification that the exposed window area has changed.
old-location: dshow\ioverlaynotify2_ondisplaychange.htm
tech.root: DirectShow
ms.assetid: 8f32a373-5d98-4491-8bfb-9445cb15ff10
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IOverlayNotify2 interface [DirectShow],OnDisplayChange method, IOverlayNotify2.OnDisplayChange, IOverlayNotify2::OnDisplayChange, IOverlayNotify2OnDisplayChange, OnDisplayChange, OnDisplayChange method [DirectShow], OnDisplayChange method [DirectShow],IOverlayNotify2 interface, dshow.ioverlaynotify2_ondisplaychange, strmif/IOverlayNotify2::OnDisplayChange
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
 - IOverlayNotify2.OnDisplayChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOverlayNotify2::OnDisplayChange


## -description



The <code>OnDisplayChange</code> method provides notification that the exposed window area has changed.




## -parameters




### -param hMonitor [in]

Handle to the monitor used for displaying the overlay.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/439b3939-84da-48f5-b2a5-47f68fedef06">IOverlayNotify2 Interface</a>
 

 

