---
UID: NF:strmif.ICaptureGraphBuilder.ControlStream
title: ICaptureGraphBuilder::ControlStream
author: windows-driver-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Sends stream control messages to the pin of the specified category on one or more capture filters in a graph.
old-location: dshow\icapturegraphbuilder_controlstream.htm
old-project: DirectShow
ms.assetid: 8d7d3a4d-3071-4829-99df-f0bcc9197b38
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ControlStream, ControlStream method [DirectShow], ControlStream method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],ControlStream method, ICaptureGraphBuilder.ControlStream, ICaptureGraphBuilder::ControlStream, ICaptureGraphBuilderControlStream, dshow.icapturegraphbuilder_controlstream, strmif/ICaptureGraphBuilder::ControlStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	ICaptureGraphBuilder.ControlStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICaptureGraphBuilder::ControlStream


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Sends stream control messages to the pin of the specified category on one or more capture filters in a graph.




## -parameters




### -param pCategory [in]

Pointer to a <b>GUID</b> specifying the output pin category. See <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a> for a list of all pin categories. This value cannot be <b>NULL</b>.


### -param pFilter [in]

Pointer to an <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface on the filter to control. Specifying <b>NULL</b> controls all capture filters in the graph. You will get one notification for each capture filter.


### -param pstart [in]

Pointer to the start time for capture. <b>NULL</b> means start now. <b>MAX_TIME</b> means cancel previous request, or take no action if there is no previous request.


### -param pstop [in]

Pointer to the stop time for capture. <b>NULL</b> means stop now. <b>MAX_TIME</b> means cancel previous request, or take no action if there is no previous request.


### -param wStartCookie [in]

Specifies a particular value to be sent when the start occurs.


### -param wStopCookie [in]

Specifies a particular value to be sent when the stop occurs.


## -returns



Returns S_FALSE if the stop notification is sent before the last sample sent by the capture filter is rendered, otherwise returns S_OK.

If this method returns S_FALSE, the application might want to wait before stopping the filter graph to allow all samples to pass through the graph and be rendered. Otherwise, samples might be lost. 



If there are no pins matching the description you provide, or if stream control cannot be supported on all of the indicated pins, this function will return a failure code. 






## -remarks



Use this method for frame-accurate capture, or for individual control of capture and preview. For example, you could turn off writing of the captured image to disk if you only want to preview the captured image.

This method uses the <a href="https://msdn.microsoft.com/126c7ed7-acc0-4248-a3ab-c91c9f1c5cee">IAMStreamControl</a> interface on the pins.

This method sends one notification for each filter found with a pin of the specified category.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

