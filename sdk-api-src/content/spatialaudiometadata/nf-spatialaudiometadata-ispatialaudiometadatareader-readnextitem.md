---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataReader.ReadNextItem
title: ISpatialAudioMetadataReader::ReadNextItem (spatialaudiometadata.h)
description: Gets the number of commands and the sample offset for the metadata item being read.
helpviewer_keywords: ["ISpatialAudioMetadataReader interface [Core Audio]","ReadNextItem method","ISpatialAudioMetadataReader.ReadNextItem","ISpatialAudioMetadataReader::ReadNextItem","ReadNextItem","ReadNextItem method [Core Audio]","ReadNextItem method [Core Audio]","ISpatialAudioMetadataReader interface","coreaudio.ispatialaudiometadatareader_readnextitem","spatialaudiometadata/ISpatialAudioMetadataReader::ReadNextItem"]
old-location: coreaudio\ispatialaudiometadatareader_readnextitem.htm
tech.root: CoreAudio
ms.assetid: AC1D5FD6-EFF1-410F-95C7-B13EACBED5D1
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataReader interface [Core Audio],ReadNextItem method, ISpatialAudioMetadataReader.ReadNextItem, ISpatialAudioMetadataReader::ReadNextItem, ReadNextItem, ReadNextItem method [Core Audio], ReadNextItem method [Core Audio],ISpatialAudioMetadataReader interface, coreaudio.ispatialaudiometadatareader_readnextitem, spatialaudiometadata/ISpatialAudioMetadataReader::ReadNextItem
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
 - ISpatialAudioMetadataReader::ReadNextItem
 - spatialaudiometadata/ISpatialAudioMetadataReader::ReadNextItem
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
 - ISpatialAudioMetadataReader.ReadNextItem
---

# ISpatialAudioMetadataReader::ReadNextItem


## -description

Gets the number of commands and the sample offset for the metadata item being read.

## -parameters

### -param commandCount [out]

Receives the number of command/value pairs in the metadata item being read.

### -param frameOffset [out]

Gets the frame offset associated with the metadata item being read.

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
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more metadata items in the frame range specified in the call to <a href="/previous-versions/windows/desktop/legacy/mt798194(v=vs.85)">ReadItemCountInFrames</a>.

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

## -remarks

Before calling <b>ReadNextItem</b>, you must open the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a> for reading by calling <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open">Open</a> after the object is created and after <a href="/windows/desktop/CoreAudio/ispatialaudiometadatawriter-close">Close</a> has been called. You must also call <a href="/previous-versions/windows/desktop/legacy/mt798194(v=vs.85)">ReadItemCountInFrames</a> before calling <b>ReadNextItem</b>.

The <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a> keeps an internal pointer to the current position within the total range of frames contained by the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> with which the reader is associated. Each call to this method causes the pointer to be advanced by the number of frames specified in the <i>readFrameCount</i> parameter.

The process for reading commands and the associated values is recursive. After each call to <b>ReadItemCountInFrames</b>, call <b>ReadNextItem</b> to get the number of commands in the next item. After every call to <b>ReadNextItem</b>, call <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-readnextitemcommand">ReadNextItemCommand</a> to read each command for the  item. Repeat this process until the entire frame range of the <b>ISpatialAudioMetadataItems</b> has been read.

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>