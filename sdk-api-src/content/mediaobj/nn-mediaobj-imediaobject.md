---
UID: NN:mediaobj.IMediaObject
title: IMediaObject
author: windows-sdk-content
description: The IMediaObject interface provides methods for manipulating a Microsoft DirectX Media Object (DMO).
old-location: dshow\imediaobject.htm
tech.root: DirectShow
ms.assetid: a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaObject, IMediaObject interface [DirectShow], IMediaObject interface [DirectShow],described, IMediaObjectInterface, dshow.imediaobject, mediaobj/IMediaObject
ms.topic: interface
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObject interface


## -description



The <code>IMediaObject</code> interface provides methods for manipulating a Microsoft DirectX Media Object (DMO).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406943(v=VS.85).aspx">AllocateStreamingResources</a>
</td>
<td align="left" width="63%">
Allocates any resources needed by the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406944(v=VS.85).aspx">Discontinuity</a>
</td>
<td align="left" width="63%">
Signals a discontinuity on the specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406945(v=VS.85).aspx">Flush</a>
</td>
<td align="left" width="63%">
Flushes all internally buffered data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406946(v=VS.85).aspx">FreeStreamingResources</a>
</td>
<td align="left" width="63%">
Frees resources allocated by the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406947(v=VS.85).aspx">GetInputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the media type that was previously set for an input stream, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406948(v=VS.85).aspx">GetInputMaxLatency</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency on a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406949(v=VS.85).aspx">GetInputSizeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements for a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406950(v=VS.85).aspx">GetInputStatus</a>
</td>
<td align="left" width="63%">
Queries whether a specified input stream can accept more input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406951(v=VS.85).aspx">GetInputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406952(v=VS.85).aspx">GetInputType</a>
</td>
<td align="left" width="63%">
Retrieves a preferred media type for a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406953(v=VS.85).aspx">GetOutputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the media type that was previously set for an output stream, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406954(v=VS.85).aspx">GetOutputSizeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements for a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406955(v=VS.85).aspx">GetOutputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406956(v=VS.85).aspx">GetOutputType</a>
</td>
<td align="left" width="63%">
Retrieves a preferred media type for a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406957(v=VS.85).aspx">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of input and output streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406958(v=VS.85).aspx">Lock</a>
</td>
<td align="left" width="63%">
Acquires or releases a lock on the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406959(v=VS.85).aspx">ProcessInput</a>
</td>
<td align="left" width="63%">
Delivers a buffer to the specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406960(v=VS.85).aspx">ProcessOutput</a>
</td>
<td align="left" width="63%">
Generates output from the current input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406961(v=VS.85).aspx">SetInputMaxLatency</a>
</td>
<td align="left" width="63%">
Sets the maximum latency on a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406962(v=VS.85).aspx">SetInputType</a>
</td>
<td align="left" width="63%">
Sets the media type on an input stream, or tests whether a particular media type is acceptable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406963(v=VS.85).aspx">SetOutputType</a>
</td>
<td align="left" width="63%">
Sets the media type on an output stream, or tests whether a particular media type is acceptable.

</td>
</tr>
</table> 

