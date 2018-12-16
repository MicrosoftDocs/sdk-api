---
UID: NN:mftransform.IMFTransform
title: IMFTransform
author: windows-sdk-content
description: Implemented by all Media Foundation Transforms (MFTs).
old-location: mf\imftransform.htm
tech.root: medfound
ms.assetid: 3cc502d8-d364-43b9-b0b6-d9474c002b20
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# IMFTransform interface


## -description


Implemented by all <a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a> (MFTs).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTransform</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/311ab66e-5dbd-452a-bad4-99a6293cbc60">AddInputStreams</a>
</td>
<td align="left" width="63%">
Adds one or more new input streams to this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cba37f7f-6ab2-469c-95c2-61d9e4d31d0b">DeleteInputStream</a>
</td>
<td align="left" width="63%">
Removes an input stream from this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb3ba2bc-550c-43b4-a69c-b546f2b92acc">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attribute store for this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed4cfdd0-28d5-4775-aa32-c17c6b13e5bf">GetInputAvailableType</a>
</td>
<td align="left" width="63%">
Retrieves a possible media type for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3603586-41fd-4eed-9942-28925ed29690">GetInputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the current media type for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6205dc1a-f209-49aa-8632-837783ef5f04">GetInputStatus</a>
</td>
<td align="left" width="63%">
Queries whether an input stream on this MFT can accept more data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2698da30-6913-41a9-9d98-f124cf31e591">GetInputStreamAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attribute store for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d57ffac7-1a92-4c6b-bd59-0acd7239c0a6">GetInputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements and other information for an input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0f75414-18cf-4e76-b875-5f373510c87b">GetOutputAvailableType</a>
</td>
<td align="left" width="63%">
Retrieves an available media type for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/433c1918-4b87-40b1-a32b-db5cdd74d769">GetOutputCurrentType</a>
</td>
<td align="left" width="63%">
Retrieves the current media type for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eb82f76-088b-4abc-9f3a-dfa5ecd1068d">GetOutputStatus</a>
</td>
<td align="left" width="63%">
Queries whether the transform is ready to produce output data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d54ce20c-8ef9-4480-9ddd-908751fc0a7e">GetOutputStreamAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attribute store for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">GetOutputStreamInfo</a>
</td>
<td align="left" width="63%">
Retrieves the buffer requirements and other information for an output stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/491f7f44-fcac-4236-ba5c-e5705267c6c2">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the current number of input and output streams on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">GetStreamIDs</a>
</td>
<td align="left" width="63%">
Retrieves the stream identifiers for the input and output streams on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d9585f0-5818-4e7f-925c-4c50ae6a6edc">GetStreamLimits</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum number of input and output streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28366df3-c414-45ff-bb15-c5483f11de85">ProcessEvent</a>
</td>
<td align="left" width="63%">
Sends an event to an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">ProcessInput</a>
</td>
<td align="left" width="63%">
Delivers data to an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6dc67e5-8473-444a-8463-24f411e59565">ProcessMessage</a>
</td>
<td align="left" width="63%">
Sends a message to the MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>
</td>
<td align="left" width="63%">
Generates output from the current input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/822a83d1-177a-4a8d-842e-eb76f8253283">SetInputType</a>
</td>
<td align="left" width="63%">
Sets, tests, or clears the media type for an input stream on this MFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/045f2f16-3f32-4cc4-9052-424f32274f34">SetOutputBounds</a>
</td>
<td align="left" width="63%">
Sets the range of timestamps the client needs for output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9a1d03f-2e56-490c-885b-78c69dea8e92">SetOutputType</a>
</td>
<td align="left" width="63%">
Sets, tests, or clears the media type for an output stream on this MFT.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

