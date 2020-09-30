---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataWriter
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter (spatialaudiometadata.h)
description: Creates an ISpatialAudioMetadataWriter object for writing spatial audio metadata items to an ISpatialAudioMetadataItems object.
helpviewer_keywords: ["ActivateSpatialAudioMetadataWriter","ActivateSpatialAudioMetadataWriter method [Core Audio]","ActivateSpatialAudioMetadataWriter method [Core Audio]","ISpatialAudioMetadataClient interface","ISpatialAudioMetadataClient interface [Core Audio]","ActivateSpatialAudioMetadataWriter method","ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataWriter","ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter","coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatawriter","spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter"]
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadatawriter.htm
tech.root: CoreAudio
ms.assetid: 0A30C838-E9B0-4CC3-BE88-9354160B8084
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioMetadataWriter, ActivateSpatialAudioMetadataWriter method [Core Audio], ActivateSpatialAudioMetadataWriter method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],ActivateSpatialAudioMetadataWriter method, ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataWriter, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadatawriter, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter
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
 - ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter
 - spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter
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
 - ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataWriter
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataWriter


## -description

Creates an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> object for writing spatial audio metadata items to an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object.

## -parameters

### -param overflowMode [in]

A value that specifies the behavior when attempting to write more metadata items to the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> than the maximum number of items specified when calling <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a>.

### -param metadataWriter [out]

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