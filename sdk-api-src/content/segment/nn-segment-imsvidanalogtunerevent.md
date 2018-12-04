---
UID: NN:segment.IMSVidAnalogTunerEvent
title: IMSVidAnalogTunerEvent
author: windows-sdk-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsvidanalogtunerevent.htm
tech.root: mstv
ms.assetid: bf1c6eb1-64c1-43cc-900c-306c01fec9cc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidAnalogTunerEvent, IMSVidAnalogTunerEvent interface [Microsoft TV Technologies], IMSVidAnalogTunerEvent interface [Microsoft TV Technologies],described, IMSVidAnalogTunerEventInterface, mstv.imsvidanalogtunerevent, segment/IMSVidAnalogTunerEvent
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
 - IMSVidAnalogTunerEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidAnalogTunerEvent interface


## -description



This topic applies to Windows XP or later.
        

The <b>IMSVidAnalogTunerEvent</b> interface is used to receive events from non-BDA analong tuners.

This interface is an outgoing connection-point interface. To receive events related to analong tuning, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://msdn.microsoft.com/432b16f1-a732-4610-9214-363b3a313a18">MSVidAnalogTunerDevice</a> object to establish a connection.




## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAnalogTunerEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/cdffe6ca-00b0-4230-963d-b4409413e5f5">IMSVidTunerEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

