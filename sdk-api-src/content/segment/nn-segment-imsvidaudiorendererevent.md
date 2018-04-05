---
UID: NN:segment.IMSVidAudioRendererEvent
title: IMSVidAudioRendererEvent
author: windows-driver-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsvidaudiorendererevent.htm
old-project: mstv
ms.assetid: 50b43d78-7df0-4b23-86c5-76655e22425f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidAudioRendererEvent, IMSVidAudioRendererEvent interface [Microsoft TV Technologies], IMSVidAudioRendererEvent interface [Microsoft TV Technologies], described, IMSVidAudioRendererEventInterface, mstv.imsvidaudiorendererevent, segment/IMSVidAudioRendererEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IMSVidAudioRendererEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidAudioRendererEvent interface


## -description



This topic applies to Windows XP or later.
        



The <b>IMSVidAudioRendererEvent</b> interface is used to receive events from the audio renderer.

This interface is an outgoing connection-point interface. To receive events related to audio rendering, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://msdn.microsoft.com/0dc7af98-5bf6-47a7-a91e-8211dd165f7c">MSVidAudioRenderer</a> object to establish a connection.


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAudioRendererEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/4f3ad7c0-02fd-4232-89f1-49517c23ee28">IMSVidOutputDeviceEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

