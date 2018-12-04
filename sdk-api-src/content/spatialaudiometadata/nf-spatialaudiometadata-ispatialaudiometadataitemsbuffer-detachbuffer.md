---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataItemsBuffer.DetachBuffer
title: ISpatialAudioMetadataItemsBuffer::DetachBuffer
author: windows-sdk-content
description: Detaches the buffer. Memory can only be attached to a single metadata item at a time.
old-location: coreaudio\ispatialaudiometadataitemsbuffer_detachbuffer.htm
tech.root: CoreAudio
ms.assetid: EE914F58-31C3-4621-987D-D0804CE90CA9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DetachBuffer, DetachBuffer method [Core Audio], DetachBuffer method [Core Audio],ISpatialAudioMetadataItemsBuffer interface, ISpatialAudioMetadataItemsBuffer interface [Core Audio],DetachBuffer method, ISpatialAudioMetadataItemsBuffer.DetachBuffer, ISpatialAudioMetadataItemsBuffer::DetachBuffer, coreaudio.ispatialaudiometadataitemsbuffer_detachbuffer, spatialaudiometadata/ISpatialAudioMetadataItemsBuffer::DetachBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudiometadata.h
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
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataItemsBuffer.DetachBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioMetadataItemsBuffer::DetachBuffer


## -description


Detaches the buffer.  Memory can only be attached to a single metadata item at a time.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_ITEMS_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> has not been opened for copying with a call to <a href="https://msdn.microsoft.com/F2D077EF-89B0-4BD6-85FB-F0AF63F1986D">Open</a> or the object has been closed for writing with a call to <a href="https://msdn.microsoft.com/891AFF53-7CAB-49FA-A8D2-CAEEB91E860F">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_ATTACH_FAILED_INTERNAL_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> was created to use a media pipeline internal buffer which can't be detached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_BUFFER_NOT_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is not attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the provided pointers is not valid.

The supplied buffer is not large enough to hold the maximum number of metadata items.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5DDD468E-0C46-4C00-BCFF-1FF7353ADB8B">ISpatialAudioMetadataItemsBuffer</a>
 

 

