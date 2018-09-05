---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataWriter.Close
title: ISpatialAudioMetadataWriter::Close
author: windows-sdk-content
description: Completes any needed operations on the metadata buffer and releases the specified ISpatialAudioMetadataItems object.
old-location: coreaudio\ispatialaudiometadatawriter_close.htm
old-project: CoreAudio
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: Close, Close method [Core Audio], Close method [Core Audio],ISpatialAudioMetadataWriter interface, ISpatialAudioMetadataWriter interface [Core Audio],Close method, ISpatialAudioMetadataWriter.Close, ISpatialAudioMetadataWriter::Close, coreaudio.ispatialaudiometadatawriter_close, spatialaudiometadata/ISpatialAudioMetadataWriter::Close
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
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioMetadataWriter.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataWriter::Close


## -description


Completes any needed operations on the metadata buffer and releases the specified <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.


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
The supplied <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> has not been opened with a call to <a href="https://msdn.microsoft.com/49B3401D-7B26-4057-81C0-6C5683B83665">Open</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_ITEMS_WRITTEN</b></dt>
</dl>
</td>
<td width="60%">
No metadata items have been written to the supplied <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_ITEM_MUST_HAVE_COMMANDS</b></dt>
</dl>
</td>
<td width="60%">
No metadata commands have been written to the supplied <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a>
 

 

