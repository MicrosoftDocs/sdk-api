---
UID: NN:mftransform.IMFDeviceTransform
title: IMFDeviceTransform (mftransform.h)
author: windows-sdk-content
description: This section contains reference information for the IMFDeviceTransform interface.
old-location: stream\imfdevicetransform.htm
tech.root: stream
ms.assetid: 375293FA-8017-4F74-A93C-C15FED8F19AF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform, IMFDeviceTransform interface [Streaming Media Devices], IMFDeviceTransform interface [Streaming Media Devices],described, mftransform/IMFDeviceTransform, stream.imfdevicetransform
ms.topic: interface
f1_keywords: 
 - "mftransform/IMFDeviceTransform"
dev_langs:
 - c++
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
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
 - mftransform.h
api_name:
 - IMFDeviceTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDeviceTransform interface


## -description


This section contains reference information for the <b>IMFDeviceTransform</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDeviceTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFDeviceTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDeviceTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-flushinputstream">FlushInputStream</a>
</td>
<td align="left" width="63%">
The <b>FlushInputStream</b> method flushes a Device MFT’s input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-flushoutputstream">FlushOutputStream</a>
</td>
<td align="left" width="63%">
The <b>FlushOutputStream</b> method flushes a Device MFT’s output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getinputavailabletype">GetInputAvailableType</a>
</td>
<td align="left" width="63%">
The <b>GetInputAvailableType</b> method gets an available media type for an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getinputcurrenttype">GetInputCurrentType</a>
</td>
<td align="left" width="63%">
The <b>GetInputCurrentType</b> method gets the current media type for an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getinputstreamattributes">GetInputStreamAttributes</a>
</td>
<td align="left" width="63%">
The <b>GetInputStreamAttributes</b> method gets the attribute store for an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getinputstreampreferredstate">GetInputStreamPreferredState</a>
</td>
<td align="left" width="63%">
The <b>GetInputStreamPreferredState</b> method gets a Device MFT input stream’s preferred state and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getinputstreamstate">GetInputStreamState</a>
</td>
<td align="left" width="63%">
The  <b>GetInputStreamState</b> method gets the Device MFT’s input stream state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getoutputavailabletype">GetOutputAvailableType</a>
</td>
<td align="left" width="63%">
The <b>GetOutputAvailableType</b> method gets an available media type for an output stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getoutputcurrenttype">GetOutputCurrentType</a>
</td>
<td align="left" width="63%">
The <b>GetOutputCurrentType</b> method gets the current media type for an output stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getoutputstreamattributes">GetOutputStreamAttributes</a>
</td>
<td align="left" width="63%">
The <b>GetOutputStreamAttributes</b> method gets the attribute store for an output stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getoutputstreamstate">GetOutputStreamState</a>
</td>
<td align="left" width="63%">
The  <b>GetOutputStreamState</b> method gets the Device MFT’s output stream state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
The <b>GetStreamCount</b> method gets the current number of input and output streams on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getstreamids">GetStreamIDs</a>
</td>
<td align="left" width="63%">
The  <b>GetStreamIDs</b> method gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-initializetransform">InitializeTransform</a>
</td>
<td align="left" width="63%">
<b>InitializeTransform</b> is called to initialize the Device MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-processevent">ProcessEvent</a>
</td>
<td align="left" width="63%">
The <b>ProcessEvent</b> method sends an event to an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-processinput">ProcessInput</a>
</td>
<td align="left" width="63%">
The <b>ProcessInput</b> method delivers data to an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-processmessage">ProcessMessage</a>
</td>
<td align="left" width="63%">
The    <b>ProcessMessage</b> method sends a message to the Device Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-processoutput">ProcessOutput</a>
</td>
<td align="left" width="63%">
The <b>ProcessOutput</b> method gets the processed output from the Device MFT output streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-setinputstreamstate">SetInputStreamState</a>
</td>
<td align="left" width="63%">
The <b>SetInputStreamState</b> method sets the Device MFT input stream state and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-setoutputstreamstate">SetOutputStreamState</a>
</td>
<td align="left" width="63%">
The <b>SetOutputStreamState</b> method sets the Device MFT output stream state and media type.

</td>
</tr>
</table> 

