---
UID: NN:mediaobj.IMediaObject
title: IMediaObject
author: windows-driver-content
description: The IMediaObject interface provides methods for manipulating a Microsoft DirectX Media Object (DMO).
old-location: dshow\imediaobject.htm
old-project: DirectShow
ms.assetid: a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMediaObject, IMediaObject interface [DirectShow], IMediaObject interface [DirectShow], described, IMediaObjectInterface, dshow.imediaobject, mediaobj/IMediaObject
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IMediaObject
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/cd608bf2-50a5-4037-aeb5-c5c380c3d6df">AllocateStreamingResources</a>
</td>
<td align="left" width="63%">
Allocates any resources needed by the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a8e51e2-5d19-423d-acd2-8f1c0a143cf3">Discontinuity</a>
</td>
<td align="left" width="63%">
Signals a discontinuity on the specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Flushes all internally buffered data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4d2dbf1-45c9-47a2-a21f-5eb04f828ec1">FreeStreamingResources</a>
</td>
<td align="left" width="63%">
Frees resources allocated by the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81d5c1b8-086c-422d-b2d7-85728507888d">GetInputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the media type that was previously set for an input stream, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8a18b4c-a59c-4e9d-aff7-62333e9ffda9">GetInputMaxLatency</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency on a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cce6359a-cd6e-46c9-a1cb-553ae5f83b9c">GetInputSizeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements for a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4581307f-cea2-4e88-81a1-972e1998c7a8">GetInputStatus</a>
</td>
<td align="left" width="63%">
Queries whether a specified input stream can accept more input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e18bf5e-cf29-4446-a1ba-422b41e02edc">GetInputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22693a22-97be-487d-ad17-31a2d8ee874c">GetInputType</a>
</td>
<td align="left" width="63%">
Retrieves a preferred media type for a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5ebcf96-d008-448e-852b-39bdf1f39c4b">GetOutputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the media type that was previously set for an output stream, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/497bc88e-4e26-409f-9d42-6a214a5d56e9">GetOutputSizeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements for a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a21e9943-4aaf-4f0e-a92a-5fcd551fe7e1">GetOutputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7652472-4091-4ecf-b623-5c6eb01be44a">GetOutputType</a>
</td>
<td align="left" width="63%">
Retrieves a preferred media type for a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05c28b44-6b92-418b-bb3f-889e59f4e0c1">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of input and output streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6923dd91-7bdb-4a0c-833d-4742973825ee">Lock</a>
</td>
<td align="left" width="63%">
Acquires or releases a lock on the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">ProcessInput</a>
</td>
<td align="left" width="63%">
Delivers a buffer to the specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">ProcessOutput</a>
</td>
<td align="left" width="63%">
Generates output from the current input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45fb0caa-cd12-4847-a646-f6fd90c50b81">SetInputMaxLatency</a>
</td>
<td align="left" width="63%">
Sets the maximum latency on a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b466fe4-97a0-46f9-9e4b-461ee66095f1">SetInputType</a>
</td>
<td align="left" width="63%">
Sets the media type on an input stream, or tests whether a particular media type is acceptable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dda3c55-d37b-4e04-9509-0e5197d6b019">SetOutputType</a>
</td>
<td align="left" width="63%">
Sets the media type on an output stream, or tests whether a particular media type is acceptable.

</td>
</tr>
</table> 

