---
UID: NN:evr.IEVRFilterConfig
title: IEVRFilterConfig
author: windows-sdk-content
description: Sets the number of input pins on the DirectShow Enhanced Video Renderer (EVR) filter.
old-location: mf\ievrfilterconfig.htm
old-project: medfound
ms.assetid: 13086d85-3dbf-4e9f-b065-d95e16412832
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 13086d85-3dbf-4e9f-b065-d95e16412832, IEVRFilterConfig, IEVRFilterConfig interface [Media Foundation], IEVRFilterConfig interface [Media Foundation],described, evr/IEVRFilterConfig, mf.ievrfilterconfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmiids.lib
-	strmiids.dll
api_name:
-	IEVRFilterConfig
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEVRFilterConfig interface


## -description


Sets the number of input pins on the DirectShow <a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer</a> (EVR) filter. To get a pointer to this interface, call <b>QueryInterface</b> on the DirectShow EVR filter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEVRFilterConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEVRFilterConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEVRFilterConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94e15032-efb6-4919-b018-953eee803135">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Retrieves the number of input pins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72777c3d-b098-43b9-80ea-ef180b7f1a4a">SetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Sets the number of input pins.

</td>
</tr>
</table> 


## -remarks



The DirectShow EVR filter starts with one input pin, which corresponds to the reference stream. To create additional pins for video substreams, call <a href="https://msdn.microsoft.com/72777c3d-b098-43b9-80ea-ef180b7f1a4a">SetNumberOfStreams</a>.

The EVR media sink for Media Foundation does not support this interface. To add new streams to the EVR media sink, call <a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">IMFMediaSink::AddStreamSink</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

