---
UID: NF:segment.IMSVidVideoRendererEvent.OverlayUnavailable
title: IMSVidVideoRendererEvent::OverlayUnavailable method
author: windows-driver-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsvidvideorendererevent_overlayunavailable.htm
old-project: mstv
ms.assetid: cb58e84f-1a45-4b72-aafd-d7a80a4b5b9d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidVideoRendererEvent, IMSVidVideoRendererEvent interface [Microsoft TV Technologies], OverlayUnavailable method, IMSVidVideoRendererEvent::OverlayUnavailable, IMSVidVideoRendererEventOverlayUnavailable, OverlayUnavailable method [Microsoft TV Technologies], OverlayUnavailable method [Microsoft TV Technologies], IMSVidVideoRendererEvent interface, OverlayUnavailable,IMSVidVideoRendererEvent.OverlayUnavailable, mstv.imsvidvideorendererevent_overlayunavailable, segment/IMSVidVideoRendererEvent::OverlayUnavailable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRendererEvent.OverlayUnavailable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRendererEvent::OverlayUnavailable method


## -description



This topic applies to Windows XP or later.
        



The <b>OverlayUnavailable</b> method is called when the overlay surface on the graphics card is not available.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The dispatch identifier (dispid) of this method is <b>eventidOverlayUnavailable</b>.




## -see-also




<a href="https://msdn.microsoft.com/ff451fa3-a755-4969-bccc-3a014865e7a9">IMSVidVideoRendererEvent Interface</a>
 

 

