---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataItemsBuffer.AttachToBuffer
title: ISpatialAudioMetadataItemsBuffer::AttachToBuffer
author: windows-sdk-content
description: Attaches caller-provided memory for storage of ISpatialAudioMetadataItems objects.
old-location: coreaudio\ispatialaudiometadataitemsbuffer_attachtobuffer.htm
old-project: CoreAudio
ms.assetid: CAB1E4C6-5572-47D0-B96F-0479773B8106
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: AttachToBuffer, AttachToBuffer method [Core Audio], AttachToBuffer method [Core Audio],ISpatialAudioMetadataItemsBuffer interface, ISpatialAudioMetadataItemsBuffer interface [Core Audio],AttachToBuffer method, ISpatialAudioMetadataItemsBuffer.AttachToBuffer, ISpatialAudioMetadataItemsBuffer::AttachToBuffer, coreaudio.ispatialaudiometadataitemsbuffer_attachtobuffer, spatialaudiometadata/ISpatialAudioMetadataItemsBuffer::AttachToBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spatialaudiometadata.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataItemsBuffer.AttachToBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataItemsBuffer::AttachToBuffer


## -description


Attaches caller-provided memory for storage of <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> objects.


## -parameters




### -param buffer [in]

A pointer to memory to use for storage.


### -param bufferLength

The length of the supplied buffer. This size must match the length required for the metadata format and maximum metadata item count.


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
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> was created to use a media pipeline internal buffer, so an external buffer can't be attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_BUFFER_ALREADY_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer has already been attached.

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
 

 

