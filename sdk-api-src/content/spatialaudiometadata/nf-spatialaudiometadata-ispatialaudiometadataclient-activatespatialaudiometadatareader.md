---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataReader
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader
author: windows-sdk-content
description: Creates an ISpatialAudioMetadataWriter object for reading spatial audio metadata items from an ISpatialAudioMetadataItems object.
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadatareader.htm
old-project: CoreAudio
ms.assetid: 3A49BB96-275A-4886-A45E-42FA7B9A6B5F
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ActivateSpatialAudioMetadataReader, ActivateSpatialAudioMetadataReader method [Core Audio], ActivateSpatialAudioMetadataReader method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],ActivateSpatialAudioMetadataReader method, ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataReader, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatareader, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader
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
 - ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader


## -description


Creates an <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> object for reading spatial audio metadata items from an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.


## -parameters




### -param metadataReader [out]

Receives a pointer to an instance of <a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>.


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

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/42EDD4D2-3DAA-4F8F-A71C-7EDFEBBCB3FB">ISpatialAudioMetadataClient</a>
 

 

