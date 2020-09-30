---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataReader
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader (spatialaudiometadata.h)
description: Creates an ISpatialAudioMetadataWriter object for reading spatial audio metadata items from an ISpatialAudioMetadataItems object.
helpviewer_keywords: ["ActivateSpatialAudioMetadataReader","ActivateSpatialAudioMetadataReader method [Core Audio]","ActivateSpatialAudioMetadataReader method [Core Audio]","ISpatialAudioMetadataClient interface","ISpatialAudioMetadataClient interface [Core Audio]","ActivateSpatialAudioMetadataReader method","ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataReader","ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader","coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatareader","spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader"]
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadatareader.htm
tech.root: CoreAudio
ms.assetid: 3A49BB96-275A-4886-A45E-42FA7B9A6B5F
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioMetadataReader, ActivateSpatialAudioMetadataReader method [Core Audio], ActivateSpatialAudioMetadataReader method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],ActivateSpatialAudioMetadataReader method, ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataReader, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatareader, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader
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
 - ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader
 - spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataReader
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataReader


## -description

Creates an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> object for reading spatial audio metadata items from an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object.

## -parameters

### -param metadataReader [out]

Receives a pointer to an instance of <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>.

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

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataclient">ISpatialAudioMetadataClient</a>