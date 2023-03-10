---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataCopier.CopyMetadataForFrames
title: ISpatialAudioMetadataCopier::CopyMetadataForFrames (spatialaudiometadata.h)
description: Copies metadata items from the source ISpatialAudioMetadataItems, provided to the Open method, object to the destination ISpatialAudioMetadataItems object, specified with the dstMetadataItems parameter.
helpviewer_keywords: ["CopyMetadataForFrames","CopyMetadataForFrames method [Core Audio]","CopyMetadataForFrames method [Core Audio]","ISpatialAudioMetadataCopier interface","ISpatialAudioMetadataCopier interface [Core Audio]","CopyMetadataForFrames method","ISpatialAudioMetadataCopier.CopyMetadataForFrames","ISpatialAudioMetadataCopier::CopyMetadataForFrames","coreaudio.ispatialaudiometadatacopier_copymetadataforframes","spatialaudiometadata/ISpatialAudioMetadataCopier::CopyMetadataForFrames"]
old-location: coreaudio\ispatialaudiometadatacopier_copymetadataforframes.htm
tech.root: CoreAudio
ms.assetid: 12ABAD23-7EDF-4F74-AE2E-26C75FA6AB37
ms.date: 12/05/2018
ms.keywords: CopyMetadataForFrames, CopyMetadataForFrames method [Core Audio], CopyMetadataForFrames method [Core Audio],ISpatialAudioMetadataCopier interface, ISpatialAudioMetadataCopier interface [Core Audio],CopyMetadataForFrames method, ISpatialAudioMetadataCopier.CopyMetadataForFrames, ISpatialAudioMetadataCopier::CopyMetadataForFrames, coreaudio.ispatialaudiometadatacopier_copymetadataforframes, spatialaudiometadata/ISpatialAudioMetadataCopier::CopyMetadataForFrames
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
 - ISpatialAudioMetadataCopier::CopyMetadataForFrames
 - spatialaudiometadata/ISpatialAudioMetadataCopier::CopyMetadataForFrames
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
 - ISpatialAudioMetadataCopier.CopyMetadataForFrames
---

# ISpatialAudioMetadataCopier::CopyMetadataForFrames


## -description

Copies metadata items from the source <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a>, provided to the <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatacopier-open">Open</a> method, object to the destination <b>ISpatialAudioMetadataItems</b> object, specified with the <i>dstMetadataItems</i> parameter.  Each call advances the internal copy position by the number of frames in the <i>copyFrameCount</i> parameter.

## -parameters

### -param copyFrameCount [in]

The number of frames from the current copy position for which metadata items are copied. After the copy, the internal copy position within the source <b>SpatialAudioMetadataItems</b> is advanced the value specified in this parameter. Set this value to 0 to copy the entire frame range contained in the  source <b>SpatialAudioMetadataItems</b>.

### -param copyMode [in]

A value that specifies the copy mode for the operation.

### -param dstMetadataItems [in]

A pointer to the  destination <b>SpatialAudioMetadataItems</b> for the copy operation.

### -param itemsCopied [out]

Receives number of metadata items copied in the operation.

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
The <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> has not been opened for copying with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatacopier-open">Open</a> or the object has been closed for writing with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatacopier-close">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the provided pointers is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a>