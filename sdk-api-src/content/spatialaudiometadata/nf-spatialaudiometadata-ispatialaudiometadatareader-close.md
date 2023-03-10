---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataReader.Close
title: ISpatialAudioMetadataReader::Close (spatialaudiometadata.h)
description: Completes any necessary operations on the SpatialAudioMetadataItems object and releases the object. (ISpatialAudioMetadataReader.Close)
helpviewer_keywords: ["Close","Close method [Core Audio]","Close method [Core Audio]","ISpatialAudioMetadataReader interface","ISpatialAudioMetadataReader interface [Core Audio]","Close method","ISpatialAudioMetadataReader.Close","ISpatialAudioMetadataReader::Close","coreaudio.ispatialaudiometadatareader_close","spatialaudiometadata/ISpatialAudioMetadataReader::Close"]
old-location: coreaudio\ispatialaudiometadatareader_close.htm
tech.root: CoreAudio
ms.assetid: A9E878E8-A319-4DB3-86A7-4499EDA567F7
ms.date: 12/05/2018
ms.keywords: Close, Close method [Core Audio], Close method [Core Audio],ISpatialAudioMetadataReader interface, ISpatialAudioMetadataReader interface [Core Audio],Close method, ISpatialAudioMetadataReader.Close, ISpatialAudioMetadataReader::Close, coreaudio.ispatialaudiometadatareader_close, spatialaudiometadata/ISpatialAudioMetadataReader::Close
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioMetadataReader::Close
 - spatialaudiometadata/ISpatialAudioMetadataReader::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataReader.Close
---

# ISpatialAudioMetadataReader::Close


## -description

Completes any necessary operations on the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">SpatialAudioMetadataItems</a> object  and releases the object.



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
The <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> has not been opened for reading with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-open">Open</a> or the object has been closed for writing with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-close">Close</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>
