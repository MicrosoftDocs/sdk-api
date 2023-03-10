---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataItems
title: ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems (spatialaudiometadata.h)
description: Creates an ISpatialAudioMetadataItems object for storing spatial audio metadata items.
helpviewer_keywords: ["ActivateSpatialAudioMetadataItems","ActivateSpatialAudioMetadataItems method [Core Audio]","ActivateSpatialAudioMetadataItems method [Core Audio]","ISpatialAudioMetadataClient interface","ISpatialAudioMetadataClient interface [Core Audio]","ActivateSpatialAudioMetadataItems method","ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataItems","ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems","coreaudio.ispatialaudiometadataclient_activatespatialaudiometadataitems","spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems"]
old-location: coreaudio\ispatialaudiometadataclient_activatespatialaudiometadataitems.htm
tech.root: CoreAudio
ms.assetid: 0788C3BE-1616-4C7B-8F47-B0C4E4034061
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioMetadataItems, ActivateSpatialAudioMetadataItems method [Core Audio], ActivateSpatialAudioMetadataItems method [Core Audio],ISpatialAudioMetadataClient interface, ISpatialAudioMetadataClient interface [Core Audio],ActivateSpatialAudioMetadataItems method, ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataItems, ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems, coreaudio.ispatialaudiometadataclient_activatespatialaudiometadataitems, spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems
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
 - ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems
 - spatialaudiometadata/ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems
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
 - ISpatialAudioMetadataClient.ActivateSpatialAudioMetadataItems
---

# ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems


## -description

Creates an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object for storing spatial audio metadata items.

## -parameters

### -param maxItemCount [in]

The maximum number of metadata items that can be stored in the returned <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a>.

### -param frameCount [in]

The valid range of frame offset positions for metadata items stored in the returned <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a>.

### -param metadataItemsBuffer [out, optional]

If a pointer is supplied, returns an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitemsbuffer">ISpatialAudioMetadataItemsBuffer</a> interface which provides methods for attaching caller-provided memory for storage of metadata items.  If this parameter is NULL, the object will allocate internal storage for the items.   This interface cannot be obtained via <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>.

### -param metadataItems [out]

Receives an instance <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object which can be populated with metadata items using an  by <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> or <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a> and can be read with an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>.

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
The pointer provided in the <i>metadataItems</i> parameter  is not valid.

The value of <i>maxItemCount</i> or <i>frameCount</i> is 0.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataclient">ISpatialAudioMetadataClient</a>