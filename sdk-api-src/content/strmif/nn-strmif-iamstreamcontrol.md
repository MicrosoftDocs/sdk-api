---
UID: NN:strmif.IAMStreamControl
title: IAMStreamControl
author: windows-sdk-content
description: The IAMStreamControl interface controls individual streams on a filter.
old-location: dshow\iamstreamcontrol.htm
old-project: DirectShow
ms.assetid: 126c7ed7-acc0-4248-a3ab-c91c9f1c5cee
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMStreamControl, IAMStreamControl interface [DirectShow], IAMStreamControl interface [DirectShow],described, IAMStreamControlInterface, dshow.iamstreamcontrol, strmif/IAMStreamControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMStreamControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMStreamControl interface


## -description



The <code>IAMStreamControl</code> interface controls individual streams on a filter. Pins on some filters expose this interface. For example, the <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux Filter</a> supports this interface on its input pins, and the <a href="https://msdn.microsoft.com/f76d5c82-33b2-4579-9420-8f97eca53ede">Audio Capture Filter</a> and <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> support it on their output pins.

This interface enables an application to turn streams on and off at specified times. For example, an application might turn off an audio stream to mute the audio during video preview. Capture applications can use this interface to specify exact start and stop times for capture, and to control capture and preview streams independently of each other.

To use this interface, call the <a href="https://msdn.microsoft.com/ce155b83-ee4a-47d4-9258-a1d18cf25f8b">IAMStreamControl::StartAt</a> method to specify when the pin will start delivering data, and the <a href="https://msdn.microsoft.com/b3dd5332-e93e-4e55-9c7f-47c302ef11a3">IAMStreamControl::StopAt</a> method to specify when it will stop delivering data. Then call <a href="https://msdn.microsoft.com/b52a5fa7-96f8-4949-9cf0-2d526f23bee1">IMediaControl::Run</a> on the Filter Graph Manager to run the filter graph. All times are relative to when the graph starts running.

When you use this interface, be aware of the following limitations:

<ul>
<li>There must be a reference clock in the filter graph.</li>
<li>Preview pins on capture cards with hardware overlay do not support this interface.</li>
<li>If you are capturing audio and video to an interleaved AVI file, the AVI Mux filter requires data both streams. If you stop one stream, the filter cannot interleave the data. For more information, see <a href="https://msdn.microsoft.com/68594752-a711-4372-95db-10947bd2ce39">IConfigInterleaving Interface</a>.</li>
</ul>
Depending on the application, you might find the <a href="https://msdn.microsoft.com/f5c91444-6ddb-403c-bff5-33d9ce91fae3">ICaptureGraphBuilder2::ControlStream</a> method more convenient, because it supports stream control at the graph level, so that you do not have to enumerate individual filters and pins.

<b>Filter developers</b>: The <a href="https://msdn.microsoft.com/a0ddc2d5-8385-4209-b1c5-9822c30f8a02">CBaseStreamControl</a> base class implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStreamControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMStreamControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMStreamControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the current streaming settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce155b83-ee4a-47d4-9258-a1d18cf25f8b">StartAt</a>
</td>
<td align="left" width="63%">
Informs the pin when to start sending streaming data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3dd5332-e93e-4e55-9c7f-47c302ef11a3">StopAt</a>
</td>
<td align="left" width="63%">
Informs the pin when to suspend processing and supplying data.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a0ddc2d5-8385-4209-b1c5-9822c30f8a02">CBaseStreamControl Class</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>
 

 

