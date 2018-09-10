---
UID: NN:mfcaptureengine.IMFCaptureEngineOnSampleCallback
title: IMFCaptureEngineOnSampleCallback
author: windows-sdk-content
description: Callback interface to receive data from the capture engine.
old-location: mf\imfcaptureengineonsamplecallback.htm
tech.root: medfound
ms.assetid: 7C621525-CCD2-45EC-9E7A-3A774B96EA6F
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFCaptureEngineOnSampleCallback, IMFCaptureEngineOnSampleCallback interface [Media Foundation], IMFCaptureEngineOnSampleCallback interface [Media Foundation],described, mf.imfcaptureengineonsamplecallback, mfcaptureengine/IMFCaptureEngineOnSampleCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngineOnSampleCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngineOnSampleCallback interface


## -description


Callback interface to receive data from the capture engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureEngineOnSampleCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFCaptureEngineOnSampleCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureEngineOnSampleCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83FEFE33-DEAD-4CE0-9EEE-B8F3801ADC1C">OnSample</a>
</td>
<td align="left" width="63%">
Called when the capture sink receives a sample.



</td>
</tr>
</table> 


## -remarks



To set the callback interface, call one of the following methods.

<ul>
<li>
<a href="https://msdn.microsoft.com/595716F6-8059-4B56-9FB3-906846BA3CBB">IMFCapturePhotoSink::SetSampleCallback</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0E14E3E4-25C7-4FCA-B220-20E346E66933">IMFCapturePreviewSink::SetSampleCallback</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1D7BB0D1-3F77-4AF3-9624-73EE4D0D0BCE">IMFCaptureRecordSink::SetSampleCallback</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

