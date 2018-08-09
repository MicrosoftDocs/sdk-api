---
UID: NN:mmstream.IMultiMediaStream
title: IMultiMediaStream
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\imultimediastream.htm
old-project: DirectShow
ms.assetid: 8be6c74f-9290-48b4-ad66-8d7d7cc94174
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IMultiMediaStream, IMultiMediaStream interface [DirectShow], IMultiMediaStream interface [DirectShow],described, IMultiMediaStreamInterface, dshow.imultimediastream, mmstream/IMultiMediaStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmstream.h
req.include-header: 
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
tech.root: 
req.typenames: STREAM_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMultiMediaStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMultiMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMultiMediaStream</code> interface is exposed by the AMMultimediaStream object. It contains methods for enumerating the media streams, retrieving information about them, and running and stopping them.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultiMediaStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMultiMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultiMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fb51794-83ac-44c5-b388-d7b945870324">EnumMediaStreams</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d8104ec-aa2a-4151-bb7f-53611d4a71f2">GetDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the multimedia stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e4f59f8-c56e-4768-9047-2793515edfeb">GetEndOfStreamEventHandle</a>
</td>
<td align="left" width="63%">
Retrieves an event that is signaled when the multimedia stream completes playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27be6104-9ca4-48d7-aeda-5b633460e252">GetInformation</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the multimedia stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d85cde4f-99f4-4641-b75f-13ca6dc7f21e">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by purpose ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d01c4cf-2de9-4e9c-8b6e-921284f4f1b6">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the multimedia stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da92c68b-176c-4773-9ae1-63f803bc206e">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>
</td>
<td align="left" width="63%">
Seeks all of the media streams to a new position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69c3612f-e91a-4ab3-8f6d-2966e64a9220">SetState</a>
</td>
<td align="left" width="63%">
Runs or stops the multimedia stream object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2f604156-68ef-4770-9929-6dbfd46c4d6d">IAMMultiMediaStream Interface</a>
 

 

