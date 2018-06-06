---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.GetSpatialAudioMetadataItemsBufferLength
title: ISpatialAudioMetadataClient::GetSpatialAudioMetadataItemsBufferLength
author: windows-sdk-content
description: Gets the length of the buffer required to store the specified number of spatial audio metadata items.
old-location: coreaudio\ispatialaudiometadataclient_getspatialaudiometadataitemsbufferlength.htm
old-project: CoreAudio
ms.assetid: 63D23390-222C-4F7E-AF8A-B49C85DFB222
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSpatialAudioMetadataItemsBufferLength, GetSpatialAudioMetadataItemsBufferLength method [Core Audio], GetSpatialAudioMetadataItemsBufferLength method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],GetSpatialAudioMetadataItemsBufferLength method, ISpatialAudioMetadataClient.GetSpatialAudioMetadataItemsBufferLength, ISpatialAudioMetadataClient::GetSpatialAudioMetadataItemsBufferLength, coreaudio.ispatialaudiometadataclient_getspatialaudiometadataitemsbufferlength, spatialaudiometadata/ISpatialAudioMetadataClient::GetSpatialAudioMetadataItemsBufferLength
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioMetadataClient.GetSpatialAudioMetadataItemsBufferLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataClient::GetSpatialAudioMetadataItemsBufferLength


## -description


Gets the length of the buffer required to store the specified number of spatial audio metadata items. Use this method to determine the correct buffer size to use when attaching caller-provided memory through the <a href="https://msdn.microsoft.com/5DDD468E-0C46-4C00-BCFF-1FF7353ADB8B">ISpatialAudioMetadataItemsBuffer</a> interface.


## -parameters




### -param maxItemCount [in]

The maximum number of metadata items to be stored in an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.


### -param bufferLength [out]

The length of the buffer required to store the number of spatial audio metadata items specified in the <i>maxItemCount</i> parameter.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The provided pointer  is not valid.

The value of <i>maxItemCount</i> or <i>frameCount</i> is 0.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/42EDD4D2-3DAA-4F8F-A71C-7EDFEBBCB3FB">ISpatialAudioMetadataClient</a>
 

 

