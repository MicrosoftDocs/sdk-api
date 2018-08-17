---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataReader.Open
title: ISpatialAudioMetadataReader::Open
author: windows-sdk-content
description: Opens an ISpatialAudioMetadataItems object for reading.
old-location: coreaudio\ispatialaudiometadatareader_open.htm
old-project: CoreAudio
ms.assetid: 50007A27-D885-47F6-9D3A-1F5B6D47BCDD
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: ISpatialAudioMetadataReader interface [Core Audio],Open method, ISpatialAudioMetadataReader.Open, ISpatialAudioMetadataReader::Open, Open, Open method [Core Audio], Open method [Core Audio],ISpatialAudioMetadataReader interface, coreaudio.ispatialaudiometadatareader_open, spatialaudiometadata/ISpatialAudioMetadataReader::Open
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
 - ISpatialAudioMetadataReader.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataReader::Open


## -description


Opens an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for reading.


## -parameters




### -param metadataItems [in]

A pointer to an  <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object to be opened for reading


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
<dt><b>SPTLAUD_MD_CLNT_E_ITEMS_ALREADY_OPEN</b></dt>
</dl>
</td>
<td width="60%">
<b>Open</b> has already been called on the supplied <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> since the object was created or since the last call to <a href="https://msdn.microsoft.com/A9E878E8-A319-4DB3-86A7-4499EDA567F7">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The provided pointer is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>
 

 

