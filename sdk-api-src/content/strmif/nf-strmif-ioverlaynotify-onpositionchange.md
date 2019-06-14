---
UID: NF:strmif.IOverlayNotify.OnPositionChange
title: IOverlayNotify::OnPositionChange (strmif.h)
author: windows-sdk-content
description: The OnPositionChange method provides notification that the position has changed.
old-location: dshow\ioverlaynotify_onpositionchange.htm
tech.root: DirectShow
ms.assetid: a5d110a6-5056-4fc1-9589-c2cc66566322
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOverlayNotify interface [DirectShow],OnPositionChange method, IOverlayNotify.OnPositionChange, IOverlayNotify::OnPositionChange, IOverlayNotifyOnPositionChange, OnPositionChange, OnPositionChange method [DirectShow], OnPositionChange method [DirectShow],IOverlayNotify interface, dshow.ioverlaynotify_onpositionchange, strmif/IOverlayNotify::OnPositionChange
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
 - IOverlayNotify.OnPositionChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlayNotify::OnPositionChange


## -description



The <code>OnPositionChange</code> method provides notification that the position has changed.




## -parameters




### -param pSourceRect [in]

Pointer to the source video rectangle.


### -param pDestinationRect [in]

Pointer to the destination video rectangle. Note that this is not clipped to the visible display area.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method is a callback intended for use by hardware overlay cards that do not want the expense of synchronous clipping updates, and just want to know when the source or destination video positions change.

Unlike the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-onclipchange">IOverlayNotify::OnClipChange</a> method, this method is not called in synchronization with the window changing but, rather, at some point after the window has changed (basically in time with WM_SIZE messages received). This is therefore suitable for overlay cards that do not inlay their data to the frame buffer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify Interface</a>
 

 

