---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataWriter.Open
title: ISpatialAudioMetadataWriter::Open
author: windows-sdk-content
description: Opens an ISpatialAudioMetadataItems object for writing.
old-location: coreaudio\ispatialaudiometadatawriter_open.htm
tech.root: CoreAudio
ms.assetid: 49B3401D-7B26-4057-81C0-6C5683B83665
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISpatialAudioMetadataWriter interface [Core Audio],Open method, ISpatialAudioMetadataWriter.Open, ISpatialAudioMetadataWriter::Open, Open, Open method [Core Audio], Open method [Core Audio],ISpatialAudioMetadataWriter interface, coreaudio.ispatialaudiometadatawriter_open, spatialaudiometadata/ISpatialAudioMetadataWriter::Open
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
 - ISpatialAudioMetadataWriter.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioMetadataWriter::Open


## -description


Opens an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for writing.


## -parameters




### -param metadataItems [in]

A pointer to an  <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object to be opened for writing.


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
<b>Open</b> has already been called on the supplied <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> since the object was created or since the last call to <a href="https://msdn.microsoft.com/2417E624-6535-49E2-9CF4-F927F731BE41">Close</a>.

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




<a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a>
 

 

