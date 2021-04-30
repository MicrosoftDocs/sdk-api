---
UID: NF:spatialaudiometadata.ISpatialAudioObjectForMetadataItems.GetSpatialAudioMetadataItems
title: ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems (spatialaudiometadata.h)
description: Gets a pointer to the ISpatialAudioMetadataItems object which stores metadata items for the ISpatialAudioObjectForMetadataItems.
helpviewer_keywords: ["GetSpatialAudioMetadataItems","GetSpatialAudioMetadataItems method [Core Audio]","GetSpatialAudioMetadataItems method [Core Audio]","ISpatialAudioObjectForMetadataItems interface","ISpatialAudioObjectForMetadataItems interface [Core Audio]","GetSpatialAudioMetadataItems method","ISpatialAudioObjectForMetadataItems.GetSpatialAudioMetadataItems","ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems","coreaudio.ispatialaudioobjectformetadataitems_getspatialaudiometadataitems","spatialaudiometadata/ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems"]
old-location: coreaudio\ispatialaudioobjectformetadataitems_getspatialaudiometadataitems.htm
tech.root: CoreAudio
ms.assetid: FD356AA9-F4BC-4864-8A9F-994EB527E123
ms.date: 12/05/2018
ms.keywords: GetSpatialAudioMetadataItems, GetSpatialAudioMetadataItems method [Core Audio], GetSpatialAudioMetadataItems method [Core Audio],ISpatialAudioObjectForMetadataItems interface, ISpatialAudioObjectForMetadataItems interface [Core Audio],GetSpatialAudioMetadataItems method, ISpatialAudioObjectForMetadataItems.GetSpatialAudioMetadataItems, ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems, coreaudio.ispatialaudioobjectformetadataitems_getspatialaudiometadataitems, spatialaudiometadata/ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems
req.header: spatialaudiometadata.h
req.include-header: Spatialaudioclient.h
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
 - ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems
 - spatialaudiometadata/ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems
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
 - ISpatialAudioObjectForMetadataItems.GetSpatialAudioMetadataItems
---

# ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems


## -description

Gets a pointer to the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object which stores metadata items for  the  <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadataitems">ISpatialAudioObjectForMetadataItems</a>.

## -parameters

### -param metadataItems [out]

Receives a pointer to the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> associated with the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadataitems">ISpatialAudioObjectForMetadataItems</a>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
</table>

## -remarks

The client must free this object when it is no longer being used by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadataitems">ISpatialAudioObjectForMetadataItems</a>