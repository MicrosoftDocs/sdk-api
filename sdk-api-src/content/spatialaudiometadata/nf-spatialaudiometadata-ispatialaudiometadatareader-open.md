---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataReader.Open
title: ISpatialAudioMetadataReader::Open (spatialaudiometadata.h)
description: Opens an ISpatialAudioMetadataItems object for reading.
helpviewer_keywords: ["ISpatialAudioMetadataReader interface [Core Audio]","Open method","ISpatialAudioMetadataReader.Open","ISpatialAudioMetadataReader::Open","Open","Open method [Core Audio]","Open method [Core Audio]","ISpatialAudioMetadataReader interface","coreaudio.ispatialaudiometadatareader_open","spatialaudiometadata/ISpatialAudioMetadataReader::Open"]
old-location: coreaudio\ispatialaudiometadatareader_open.htm
tech.root: CoreAudio
ms.assetid: 50007A27-D885-47F6-9D3A-1F5B6D47BCDD
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataReader interface [Core Audio],Open method, ISpatialAudioMetadataReader.Open, ISpatialAudioMetadataReader::Open, Open, Open method [Core Audio], Open method [Core Audio],ISpatialAudioMetadataReader interface, coreaudio.ispatialaudiometadatareader_open, spatialaudiometadata/ISpatialAudioMetadataReader::Open
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
 - ISpatialAudioMetadataReader::Open
 - spatialaudiometadata/ISpatialAudioMetadataReader::Open
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
 - ISpatialAudioMetadataReader.Open
---

# ISpatialAudioMetadataReader::Open


## -description

Opens an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object for reading.

## -parameters

### -param metadataItems [in]

A pointer to an  <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object to be opened for reading

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
<b>Open</b> has already been called on the supplied <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> since the object was created or since the last call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-close">Close</a>.

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

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>