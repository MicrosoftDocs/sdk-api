---
UID: NN:mediaobj.IMediaObject
title: IMediaObject (mediaobj.h)
description: The IMediaObject interface provides methods for manipulating a Microsoft DirectX Media Object (DMO).helpviewer_keywords: ["IMediaObject","IMediaObject interface [DirectShow]","IMediaObject interface [DirectShow]","described","IMediaObjectInterface","dshow.imediaobject","mediaobj/IMediaObject"]
old-location: dshow\imediaobject.htm
tech.root: DirectShow
ms.assetid: a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b
ms.date: 12/05/2018
ms.keywords: IMediaObject, IMediaObject interface [DirectShow], IMediaObject interface [DirectShow],described, IMediaObjectInterface, dshow.imediaobject, mediaobj/IMediaObject
f1_keywords:
- mediaobj/IMediaObject
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaObject interface


## -description



The <code>IMediaObject</code> interface provides methods for manipulating a Microsoft DirectX Media Object (DMO).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaObject</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources">AllocateStreamingResources</a>
</td>
<td align="left" width="63%">
Allocates any resources needed by the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity">Discontinuity</a>
</td>
<td align="left" width="63%">
Signals a discontinuity on the specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush">Flush</a>
</td>
<td align="left" width="63%">
Flushes all internally buffered data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources">FreeStreamingResources</a>
</td>
<td align="left" width="63%">
Frees resources allocated by the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype">GetInputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the media type that was previously set for an input stream, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency">GetInputMaxLatency</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency on a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo">GetInputSizeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements for a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputstatus">GetInputStatus</a>
</td>
<td align="left" width="63%">
Queries whether a specified input stream can accept more input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo">GetInputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype">GetInputType</a>
</td>
<td align="left" width="63%">
Retrieves a preferred media type for a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype">GetOutputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the media type that was previously set for an output stream, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo">GetOutputSizeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements for a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo">GetOutputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype">GetOutputType</a>
</td>
<td align="left" width="63%">
Retrieves a preferred media type for a specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of input and output streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock">Lock</a>
</td>
<td align="left" width="63%">
Acquires or releases a lock on the DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput">ProcessInput</a>
</td>
<td align="left" width="63%">
Delivers a buffer to the specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">ProcessOutput</a>
</td>
<td align="left" width="63%">
Generates output from the current input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency">SetInputMaxLatency</a>
</td>
<td align="left" width="63%">
Sets the maximum latency on a specified input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype">SetInputType</a>
</td>
<td align="left" width="63%">
Sets the media type on an input stream, or tests whether a particular media type is acceptable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype">SetOutputType</a>
</td>
<td align="left" width="63%">
Sets the media type on an output stream, or tests whether a particular media type is acceptable.

</td>
</tr>
</table> 

