---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorGetBehaviorHints
title: ID3D11VideoContext1::VideoProcessorGetBehaviorHints
author: windows-sdk-content
description: Returns driver hints that indicate which of the video processor operations are best performed using multi-plane overlay hardware rather than ID3D11VideoContext::VideoProcessorBlt method.
old-location: mf\id3d11videocontext1_videoprocessorgetbehaviorhints.htm
tech.root: medfound
ms.assetid: DDA8B3DE-A9D2-48A5-ABEE-E3F7A0EEB965
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorGetBehaviorHints method, ID3D11VideoContext1.VideoProcessorGetBehaviorHints, ID3D11VideoContext1::VideoProcessorGetBehaviorHints, VideoProcessorGetBehaviorHints, VideoProcessorGetBehaviorHints method [Media Foundation], VideoProcessorGetBehaviorHints method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorGetBehaviorHints, mf.id3d11videocontext1_videoprocessorgetbehaviorhints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.VideoProcessorGetBehaviorHints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11_1.h
: 
- ID3D11VideoContext1.VideoProcessorGetBehaviorHints
: 
---

# ID3D11VideoContext1::VideoProcessorGetBehaviorHints


## -description


Returns driver hints that indicate which of the video processor operations are best performed using multi-plane overlay hardware rather than <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> method.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param OutputWidth [in]

Type: <b>UINT</b>

The width of the output stream.


### -param OutputHeight [in]

Type: <b>UINT</b>

The height of the output stream.


### -param OutputFormat [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The format of the output stream.


### -param StreamCount [in]

Type: <b>UINT</b>

The number of input streams to process.


### -param pStreams [in]

Type: <b>const <a href="https://msdn.microsoft.com/0B90AB2C-3F62-49FF-A1DB-FCB07A33F482">D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT</a>*</b>

An array of structures that specifies the format of each input stream and whether each stream should be used when computing behavior hints.


### -param pBehaviorHints [out]

Type: <b>UINT*</b>

A pointer to a bitwise OR combination of <a href="https://msdn.microsoft.com/0EB7F918-EA7A-4E7E-9B6D-53F582CC6B28">D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS</a> values indicating which video processor operations would best be performed using multi-plane overlay hardware rather than the <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> method.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is insufficient memory to complete the operation.</td>
</tr>
</table>
 




## -remarks



This method computes the behavior hints using the current state of the video processor as set by the "SetOutput" and "SetStream" methods of <a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a> and <a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>. You must set the proper state before calling this method to ensure that the returned hints contain useful data.




## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

