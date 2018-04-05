---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataCopier
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier method
author: windows-driver-content
description: Creates an ISpatialAudioMetadataWriter object for copying spatial audio metadata items from one ISpatialAudioMetadataItems object to another.
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadatacopier.htm
old-project: CoreAudio
ms.assetid: 52534220-65A0-46BE-9A05-E00B84170382
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: ActivateSpatialAudioMetadataCopier method [Core Audio], ActivateSpatialAudioMetadataCopier method [Core Audio], ISpatialAudioMetadataClient interface, ActivateSpatialAudioMetadataCopier,ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataCopier, ISpatialAudioMetadataClient, ISpatialAudioMetadataClient interface [Core Audio], ActivateSpatialAudioMetadataCopier method, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatacopier, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier
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
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	spatialaudiometadata.h
api_name:
-	ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataCopier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier method


## -description


Creates an <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> object for copying spatial audio metadata items from one <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object to another.


## -parameters




### -param metadataCopier [out]

Receives a pointer to an instance of <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a>.


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
 

 

