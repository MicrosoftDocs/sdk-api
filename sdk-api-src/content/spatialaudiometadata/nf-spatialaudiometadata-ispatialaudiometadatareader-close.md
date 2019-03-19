---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataReader.Close
title: ISpatialAudioMetadataReader::Close (spatialaudiometadata.h)
author: windows-sdk-content
description: Completes any necessary operations on the SpatialAudioMetadataItems object and releases the object.
old-location: coreaudio\ispatialaudiometadatareader_close.htm
tech.root: CoreAudio
ms.assetid: A9E878E8-A319-4DB3-86A7-4499EDA567F7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Close, Close method [Core Audio], Close method [Core Audio],ISpatialAudioMetadataReader interface, ISpatialAudioMetadataReader interface [Core Audio],Close method, ISpatialAudioMetadataReader.Close, ISpatialAudioMetadataReader::Close, coreaudio.ispatialaudiometadatareader_close, spatialaudiometadata/ISpatialAudioMetadataReader::Close
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
 - ISpatialAudioMetadataReader.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioMetadataReader::Close


## -description


Completes any necessary operations on the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">SpatialAudioMetadataItems</a> object  and releases the object.


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
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> has not been opened for reading with a call to <a href="https://msdn.microsoft.com/50007A27-D885-47F6-9D3A-1F5B6D47BCDD">Open</a> or the object has been closed for writing with a call to <a href="https://msdn.microsoft.com/A9E878E8-A319-4DB3-86A7-4499EDA567F7">Close</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>
 

 

