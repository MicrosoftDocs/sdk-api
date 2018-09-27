---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataWriter
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter
author: windows-sdk-content
description: Creates an ISpatialAudioMetadataWriter object for writing spatial audio metadata items to an ISpatialAudioMetadataItems object.
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadatawriter.htm
tech.root: CoreAudio
ms.assetid: 0A30C838-E9B0-4CC3-BE88-9354160B8084
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ActivateSpatialAudioMetadataWriter, ActivateSpatialAudioMetadataWriter method [Core Audio], ActivateSpatialAudioMetadataWriter method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],ActivateSpatialAudioMetadataWriter method, ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataWriter, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatawriter, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter
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
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter


## -description


Creates an <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> object for writing spatial audio metadata items to an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.


## -parameters




### -param overflowMode [in]

A value that specifies the behavior when attempting to write more metadata items to the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> than the maximum number of items specified when calling <a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ActivateSpatialAudioMetadataItems</a>.


### -param metadataWriter [out]

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
 

 

