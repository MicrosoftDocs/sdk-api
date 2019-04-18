---
UID: NN:mmstream.IMultiMediaStream
title: IMultiMediaStream (mmstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\imultimediastream.htm
tech.root: DirectShow
ms.assetid: 8be6c74f-9290-48b4-ad66-8d7d7cc94174
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMultiMediaStream, IMultiMediaStream interface [DirectShow], IMultiMediaStream interface [DirectShow],described, IMultiMediaStreamInterface, dshow.imultimediastream, mmstream/IMultiMediaStream
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Dd390326(v=VS.85).aspx">EnumMediaStreams</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390327(v=VS.85).aspx">GetDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the multimedia stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390328(v=VS.85).aspx">GetEndOfStreamEventHandle</a>
</td>
<td align="left" width="63%">
Retrieves an event that is signaled when the multimedia stream completes playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390329(v=VS.85).aspx">GetInformation</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the multimedia stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390330(v=VS.85).aspx">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by purpose ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390331(v=VS.85).aspx">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the multimedia stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390332(v=VS.85).aspx">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390334(v=VS.85).aspx">Seek</a>
</td>
<td align="left" width="63%">
Seeks all of the media streams to a new position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390335(v=VS.85).aspx">SetState</a>
</td>
<td align="left" width="63%">
Runs or stops the multimedia stream object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd319688(v=VS.85).aspx">IAMMultiMediaStream Interface</a>
 

 

