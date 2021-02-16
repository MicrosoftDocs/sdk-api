---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataCopier.Open
title: ISpatialAudioMetadataCopier::Open (spatialaudiometadata.h)
description: Opens an ISpatialAudioMetadataItems object for copying.
helpviewer_keywords: ["ISpatialAudioMetadataCopier interface [Core Audio]","Open method","ISpatialAudioMetadataCopier.Open","ISpatialAudioMetadataCopier::Open","Open","Open method [Core Audio]","Open method [Core Audio]","ISpatialAudioMetadataCopier interface","coreaudio.ispatialaudiometadatacopier_open","spatialaudiometadata/ISpatialAudioMetadataCopier::Open"]
old-location: coreaudio\ispatialaudiometadatacopier_open.htm
tech.root: CoreAudio
ms.assetid: F2D077EF-89B0-4BD6-85FB-F0AF63F1986D
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataCopier interface [Core Audio],Open method, ISpatialAudioMetadataCopier.Open, ISpatialAudioMetadataCopier::Open, Open, Open method [Core Audio], Open method [Core Audio],ISpatialAudioMetadataCopier interface, coreaudio.ispatialaudiometadatacopier_open, spatialaudiometadata/ISpatialAudioMetadataCopier::Open
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
 - ISpatialAudioMetadataCopier::Open
 - spatialaudiometadata/ISpatialAudioMetadataCopier::Open
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
 - ISpatialAudioMetadataCopier.Open
---

# ISpatialAudioMetadataCopier::Open


## -description

Opens an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object for copying.

## -parameters

### -param metadataItems [in]

A pointer to an  <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object to be opened for copying

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
<b>Open</b> has already been called on the supplied <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> since the object was created or since the last call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatacopier-close">Close</a>.

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

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a>



<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>