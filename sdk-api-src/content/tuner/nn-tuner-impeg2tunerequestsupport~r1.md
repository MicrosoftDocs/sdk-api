---
UID: NN:tuner.IMPEG2TuneRequestSupport~r1
title: IMPEG2TuneRequestSupport
author: windows-sdk-content
description: TBD
tech.root:
ms.assetid: b7381962-b76e-4041-a080-66408d0f3cb7
ms.author: windowssdkdev
ms.date: 
ms.topic: interface
req.header: tuner.h
req.include-header:
req.redist:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library: 
topic_type: 
 - apiref
api_type: 
 - COM
api_location: 
 - tuner.h
api_name: 
 - IMPEG2TuneRequestSupport
product: Windows
targetos: Windows
---

# IMPEG2TuneRequestSupport interface

## -description

Indicates that the default network provider for a tuning space allows tuning through the <a href="https://msdn.microsoft.com/a9e37b8b-9272-43c6-b36e-1e82b0d1b0db">IMPEG2TuneRequest</a> interface as well as tuning through the native tuning request type implemented by that tuning space's <a href="https://msdn.microsoft.com/513d4d3e-47df-4a12-80ce-9fc1400af176">CreateTuneRequest</a> method.

For example, the <a href="https://msdn.microsoft.com/3414b1b7-21d4-4d10-b487-d6886ef36c7b">DVBTuningSpace</a> object implements the <b>IMPEG2TuneRequestSupport</b> interface. This indicates that the default network provider for the <b>DVBTuningSpace</b> object supports tuning through both the object's native <a href="https://msdn.microsoft.com/513d4d3e-47df-4a12-80ce-9fc1400af176">IDVBTuneRequest::CreateTuneRequest</a> method and the <b>IMPEG2TuneRequest::CreateTuneRequest</b> method. (In both cases, the tune request interfaces inherit the <b>CreateTuneRequest</b> method from the  <a href="https://msdn.microsoft.com/e5cb1a15-29c4-4e0f-aed2-eafe12ea007a">ITuneRequest</a> interface).

The following tuning space objects support the <b>IMPEG2TuneRequestSupport</b> interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/32966f5c-54c2-4cba-a3c1-aa7bb729892a">DVBSTuningSpace</a> object</li>
<li>
<a href="https://msdn.microsoft.com/3414b1b7-21d4-4d10-b487-d6886ef36c7b">DVBTuningSpace</a> object</li>
<li>
<a href="https://msdn.microsoft.com/8535a8c3-35df-4c6c-872a-437f5c7a2e56">ATSCTuningSpace</a> object</li>
</ul>


## -inheritance
IMPEG2TuneRequestSupport interits from . 
## -members

	The IMPEG2TuneRequestSupport has no additional methods.

## -remarks


To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestSupport)</code>.



## -see-also