---
UID: NN:mftransform.IMFDeviceTransform
title: IMFDeviceTransform
author: windows-sdk-content
description: This section contains reference information for the IMFDeviceTransform interface.
old-location: stream\imfdevicetransform.htm
tech.root: stream
ms.assetid: 375293FA-8017-4F74-A93C-C15FED8F19AF
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMFDeviceTransform, IMFDeviceTransform interface [Streaming Media Devices], IMFDeviceTransform interface [Streaming Media Devices],described, mftransform/IMFDeviceTransform, stream.imfdevicetransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDeviceTransform interface


## -description


This section contains reference information for the <b>IMFDeviceTransform</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDeviceTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFDeviceTransform</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/646A9446-B87A-40B5-8A0F-9DE67286825B">FlushInputStream</a>
</td>
<td align="left" width="63%">
The <b>FlushInputStream</b> method flushes a Device MFT’s input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/261CA606-2813-4FE4-955D-6AEA338EC0FC">FlushOutputStream</a>
</td>
<td align="left" width="63%">
The <b>FlushOutputStream</b> method flushes a Device MFT’s output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F3DA67A-AC31-43A5-83AF-7744F6AA5810">GetInputAvailableType</a>
</td>
<td align="left" width="63%">
The <b>GetInputAvailableType</b> method gets an available media type for an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E2955AD-ECBD-4C24-972A-8F670DC08F0F">GetInputCurrentType</a>
</td>
<td align="left" width="63%">
The <b>GetInputCurrentType</b> method gets the current media type for an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/087696C2-BD29-4BAE-8285-1B127E0D076E">GetInputStreamAttributes</a>
</td>
<td align="left" width="63%">
The <b>GetInputStreamAttributes</b> method gets the attribute store for an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56334B73-DCBC-4999-9685-2489D6C15E2E">GetInputStreamPreferredState</a>
</td>
<td align="left" width="63%">
The <b>GetInputStreamPreferredState</b> method gets a Device MFT input stream’s preferred state and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B5319512-EC6C-4940-881E-3DB1CA7BF0E3">GetInputStreamState</a>
</td>
<td align="left" width="63%">
The  <b>GetInputStreamState</b> method gets the Device MFT’s input stream state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B4224C70-5864-4AE3-8388-2B9A62517B62">GetOutputAvailableType</a>
</td>
<td align="left" width="63%">
The <b>GetOutputAvailableType</b> method gets an available media type for an output stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ABDDED13-5C35-4030-838B-92BECA23F6A2">GetOutputCurrentType</a>
</td>
<td align="left" width="63%">
The <b>GetOutputCurrentType</b> method gets the current media type for an output stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ABC8699B-0DFB-401B-9DB2-F3EBA5A64C8B">GetOutputStreamAttributes</a>
</td>
<td align="left" width="63%">
The <b>GetOutputStreamAttributes</b> method gets the attribute store for an output stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A79FC296-7D18-4C74-97E0-F37475AB90D5">GetOutputStreamState</a>
</td>
<td align="left" width="63%">
The  <b>GetOutputStreamState</b> method gets the Device MFT’s output stream state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6FD4B393-05E6-4400-B1A3-D69B7F1B90F0">GetStreamCount</a>
</td>
<td align="left" width="63%">
The <b>GetStreamCount</b> method gets the current number of input and output streams on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/378A8E3F-8B1E-4C0B-9C30-FE78E1939422">GetStreamIDs</a>
</td>
<td align="left" width="63%">
The  <b>GetStreamIDs</b> method gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02ACBC34-0514-4EAE-AC48-62F6AE219E93">InitializeTransform</a>
</td>
<td align="left" width="63%">
<b>InitializeTransform</b> is called to initialize the Device MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E8B208C-A492-41C8-9A86-34B11375053B">ProcessEvent</a>
</td>
<td align="left" width="63%">
The <b>ProcessEvent</b> method sends an event to an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB4197BA-5963-45E7-B196-94F907637EBB">ProcessInput</a>
</td>
<td align="left" width="63%">
The <b>ProcessInput</b> method delivers data to an input stream on this Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/890CAC55-CF9E-420C-ACFC-5A92E53258AA">ProcessMessage</a>
</td>
<td align="left" width="63%">
The    <b>ProcessMessage</b> method sends a message to the Device Media Foundation transform (MFT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A99242D6-5225-493C-A5A8-CFDBB49D01A0">ProcessOutput</a>
</td>
<td align="left" width="63%">
The <b>ProcessOutput</b> method gets the processed output from the Device MFT output streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/010E482E-7464-45AE-80B6-9456864E1C96">SetInputStreamState</a>
</td>
<td align="left" width="63%">
The <b>SetInputStreamState</b> method sets the Device MFT input stream state and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E44A5D0C-440A-4929-9640-AD2F7AA7D19F">SetOutputStreamState</a>
</td>
<td align="left" width="63%">
The <b>SetOutputStreamState</b> method sets the Device MFT output stream state and media type.

</td>
</tr>
</table> 

