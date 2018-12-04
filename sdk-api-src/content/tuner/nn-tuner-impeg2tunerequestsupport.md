---
UID: NN:tuner.IMPEG2TuneRequestSupport
title: IMPEG2TuneRequestSupport
author: windows-sdk-content
description: Indicates that the default network provider for a tuning space allows tuning through the IMPEG2TuneRequest interface as well as tuning through the native tuning request type implemented by that tuning space's CreateTuneRequest method.
old-location: mstv\impeg2tunerequestsupport.htm
tech.root: mstv
ms.assetid: 22ba436f-8ccf-4f78-b33c-2328bd495df6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMPEG2TuneRequestSupport, IMPEG2TuneRequestSupport interface [Microsoft TV Technologies], IMPEG2TuneRequestSupport interface [Microsoft TV Technologies],described, mstv.impeg2tunerequestsupport, tuner/IMPEG2TuneRequestSupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IMPEG2TuneRequestSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestSupport)</code>.



