---
UID: NN:segment.IMSVidFilePlaybackEvent
title: IMSVidFilePlaybackEvent (segment.h)
author: windows-sdk-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsvidfileplaybackevent.htm
tech.root: mstv
ms.assetid: 7dd435a1-8cd4-45c5-8250-770b629d3f3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlaybackEvent, IMSVidFilePlaybackEvent interface [Microsoft TV Technologies], IMSVidFilePlaybackEvent interface [Microsoft TV Technologies],described, IMSVidFilePlaybackEventInterface, mstv.imsvidfileplaybackevent, segment/IMSVidFilePlaybackEvent
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidFilePlaybackEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidFilePlaybackEvent interface


## -description



This topic applies to Windows XP or later.
        



The <b>IMSVidFilePlaybackEvent</b> interface is used to receive events from the file playback object.

This interface is an outgoing connection-point interface. To receive events related to file playback, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://msdn.microsoft.com/da8a1d86-b3a5-4488-8bbc-82dd09aeeaca">MSVidFilePlaybackDevice</a> object to establish a connection.


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFilePlaybackEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694587(v=VS.85).aspx">IMSVidPlaybackEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

