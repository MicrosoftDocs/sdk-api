---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MFCreateSampleCopierMFT function


## -description


Creates an instance of the sample copier transform.


## -parameters




### -param ppCopierMFT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The sample copier is a Media Foundation transform (MFT) that copies data from input samples to output samples without modifying the data. The following data is copied from the sample:

<ul>
<li>All <a href="https://msdn.microsoft.com/64aead5a-61c4-4e83-a556-af33e0aa82be">Sample Attributes</a>.</li>
<li>The time stamp and duration.</li>
<li>Sample flags (see <a href="https://msdn.microsoft.com/30dac293-981b-41f3-951d-186d6a603d0a">IMFSample::SetSampleFlags</a>).</li>
<li>The data in the media buffers. If the input sample contains multiple buffers, the data is copied into a single buffer on the output sample.</li>
</ul>
This MFT is useful in the following situation:

<ul>
<li>One pipeline object, such as a media source, allocates media samples for output.</li>
<li>Another pipeline object, such as a media sink, allocates its own media samples for input. For example, the object might require buffers allocated from a special memory pool, such as video memory.</li>
</ul>
The following diagram shows this situation with a media source and a media sink.

<img alt="Diagram: Media Source points to a Sample; Media Sink points to a second Sample; Sample Copier points to an arrow from the first sample to the second" src="images/SampleCopierMFT.gif"/>

In order for the media sink to receive data from the media source, the data must be copied into the media samples owned by the media sink. The sample copier can be used for this purpose.

A specific example of such a media sink is the  <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR). The EVR allocates samples that contain Direct3D surface buffers, so it cannot receive video samples directly from a media source. Starting in Windows 7, the topology loader automatically handles this case by inserting the sample copier between the media source and the EVR.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

