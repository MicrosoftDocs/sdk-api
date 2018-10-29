---
UID: NN:mfidl.IMFMediaSink
title: IMFMediaSink
author: windows-sdk-content
description: Implemented by media sink objects.
old-location: mf\imfmediasink.htm
tech.root: medfound
ms.assetid: 103e6fd8-a18f-480a-8261-099623014659
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 103e6fd8-a18f-480a-8261-099623014659, IMFMediaSink, IMFMediaSink interface [Media Foundation], IMFMediaSink interface [Media Foundation],described, mf.imfmediasink, mfidl/IMFMediaSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSink interface


## -description


Implemented by media sink objects. This interface is the base interface for all Media Foundation media sinks. Stream sinks handle the actual processing of data on each stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">AddStreamSink</a>
</td>
<td align="left" width="63%">
Adds a new stream sink to the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7e8e2af-8b10-47f5-8b09-a7147ace5ba1">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Gets the characteristics of the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffa6a7b5-cd79-4c45-a5e3-9d133ffc89a6">GetPresentationClock</a>
</td>
<td align="left" width="63%">
Gets the presentation clock that was set on the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/267a8efc-6743-48ca-a1c4-da82f3770419">GetStreamSinkById</a>
</td>
<td align="left" width="63%">
Gets a stream sink, specified by stream identifier.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01604801-1566-410c-b23a-0568c7298868">GetStreamSinkByIndex</a>
</td>
<td align="left" width="63%">
Gets a stream sink, specified by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf4b5713-586c-4b12-80a1-4452eec63e32">GetStreamSinkCount</a>
</td>
<td align="left" width="63%">
Gets the number of stream sinks on this media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f99ee960-7fea-4867-bc24-d7e1d6fcafa5">RemoveStreamSink</a>
</td>
<td align="left" width="63%">
Removes a stream sink from the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/844fc3b3-b56e-4048-b589-e24457bcc419">SetPresentationClock</a>
</td>
<td align="left" width="63%">
Sets the presentation clock on the media sink.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the media sink and releases the resources it is using.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

