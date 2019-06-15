---
UID: NN:mftransform.IMFTransform
title: IMFTransform (mftransform.h)
author: windows-sdk-content
description: Implemented by all Media Foundation Transforms (MFTs).
old-location: mf\imftransform.htm
tech.root: medfound
ms.assetid: 3cc502d8-d364-43b9-b0b6-d9474c002b20
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3cc502d8-d364-43b9-b0b6-d9474c002b20, IMFTransform, IMFTransform interface [Media Foundation], IMFTransform interface [Media Foundation],described, mf.imftransform, mftransform/IMFTransform
ms.topic: interface
req.header: mftransform.h
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
 - IMFTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTransform interface


## -description


Implemented by all <a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a> (MFTs).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams">AddInputStreams</a>
</td>
<td align="left" width="63%">
Adds one or more new input streams to this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream">DeleteInputStream</a>
</td>
<td align="left" width="63%">
Removes an input stream from this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attribute store for this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype">GetInputAvailableType</a>
</td>
<td align="left" width="63%">
Retrieves a possible media type for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype">GetInputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the current media type for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus">GetInputStatus</a>
</td>
<td align="left" width="63%">
Queries whether an input stream on this MFT can accept more data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes">GetInputStreamAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attribute store for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo">GetInputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements and other information for an input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype">GetOutputAvailableType</a>
</td>
<td align="left" width="63%">
Retrieves an available media type for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype">GetOutputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the current media type for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus">GetOutputStatus</a>
</td>
<td align="left" width="63%">
Queries whether the transform is ready to produce output data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes">GetOutputStreamAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attribute store for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">GetOutputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements and other information for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the current number of input and output streams on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">GetStreamIDs</a>
</td>
<td align="left" width="63%">
Retrieves the stream identifiers for the input and output streams on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits">GetStreamLimits</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum number of input and output streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent">ProcessEvent</a>
</td>
<td align="left" width="63%">
Sends an event to an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a>
</td>
<td align="left" width="63%">
Delivers data to an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage">ProcessMessage</a>
</td>
<td align="left" width="63%">
Sends a message to the MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>
</td>
<td align="left" width="63%">
Generates output from the current input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype">SetInputType</a>
</td>
<td align="left" width="63%">
Sets, tests, or clears the media type for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds">SetOutputBounds</a>
</td>
<td align="left" width="63%">
Sets the range of timestamps the client needs for output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype">SetOutputType</a>
</td>
<td align="left" width="63%">
Sets, tests, or clears the media type for an output stream on this MFT.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
 

 

