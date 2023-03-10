---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataCopier
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier (spatialaudiometadata.h)
description: Creates an ISpatialAudioMetadataWriter object for copying spatial audio metadata items from one ISpatialAudioMetadataItems object to another.
helpviewer_keywords: ["ActivateSpatialAudioMetadataCopier","ActivateSpatialAudioMetadataCopier method [Core Audio]","ActivateSpatialAudioMetadataCopier method [Core Audio]","ISpatialAudioMetadataClient interface","ISpatialAudioMetadataClient interface [Core Audio]","ActivateSpatialAudioMetadataCopier method","ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataCopier","ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier","coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatacopier","spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier"]
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadatacopier.htm
tech.root: CoreAudio
ms.assetid: 52534220-65A0-46BE-9A05-E00B84170382
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioMetadataCopier, ActivateSpatialAudioMetadataCopier method [Core Audio], ActivateSpatialAudioMetadataCopier method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],ActivateSpatialAudioMetadataCopier method, ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataCopier, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatacopier, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier
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
 - ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier
 - spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier
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
 - ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataCopier
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataCopier


## -description

Creates an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> object for copying spatial audio metadata items from one <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object to another.

## -parameters

### -param metadataCopier [out]

Receives a pointer to an instance of <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>.

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