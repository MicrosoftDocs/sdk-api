---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataItems
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems
author: windows-driver-content
description: Creates an ISpatialAudioMetadataItems object for storing spatial audio metadata items.
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadataitems.htm
old-project: CoreAudio
ms.assetid: 0788C3BE-1616-4C7B-8F47-B0C4E4034061
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ActivateSpatialAudioMetadataItems, ActivateSpatialAudioMetadataItems method [Core Audio], ActivateSpatialAudioMetadataItems method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],ActivateSpatialAudioMetadataItems method, ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataItems, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadataitems, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems
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
-	ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems


## -description


Creates an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for storing spatial audio metadata items.


## -parameters




### -param maxItemCount [in]

The maximum number of metadata items that can be stored in the returned <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>.


### -param frameCount [in]

The valid range of frame offset positions for metadata items stored in the returned <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>.


### -param metadataItemsBuffer [out, optional]

If a pointer is supplied, returns an <a href="https://msdn.microsoft.com/5DDD468E-0C46-4C00-BCFF-1FF7353ADB8B">ISpatialAudioMetadataItemsBuffer</a> interface which provides methods for attaching caller-provided memory for storage of metadata items.  If this parameter is NULL, the object will allocate internal storage for the items.   This interface cannot be obtained via <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>.


### -param metadataItems [out]

Receives an instance <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object which can be populated with metadata items using an  by <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> or <a href="https://msdn.microsoft.com/74708744-78BF-4135-BB0A-50A7CA41ECDD">ISpatialAudioMetadataCopier</a> and can be read with an <a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>.


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
The pointer provided in the <i>metadataItems</i> parameter  is not valid.

The value of <i>maxItemCount</i> or <i>frameCount</i> is 0.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/42EDD4D2-3DAA-4F8F-A71C-7EDFEBBCB3FB">ISpatialAudioMetadataClient</a>
 

 

