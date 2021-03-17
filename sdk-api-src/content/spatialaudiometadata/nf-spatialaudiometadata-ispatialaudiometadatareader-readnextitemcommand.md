---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataReader.ReadNextItemCommand
title: ISpatialAudioMetadataReader::ReadNextItemCommand (spatialaudiometadata.h)
description: Reads metadata commands and value data for the current item.
helpviewer_keywords: ["ISpatialAudioMetadataReader interface [Core Audio]","ReadNextItemCommand method","ISpatialAudioMetadataReader.ReadNextItemCommand","ISpatialAudioMetadataReader::ReadNextItemCommand","ReadNextItemCommand","ReadNextItemCommand method [Core Audio]","ReadNextItemCommand method [Core Audio]","ISpatialAudioMetadataReader interface","coreaudio.ispatialaudiometadatareader_readnextitemcommand","spatialaudiometadata/ISpatialAudioMetadataReader::ReadNextItemCommand"]
old-location: coreaudio\ispatialaudiometadatareader_readnextitemcommand.htm
tech.root: CoreAudio
ms.assetid: 9B58546A-FBE3-47CD-8E5F-63D0C5608F00
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataReader interface [Core Audio],ReadNextItemCommand method, ISpatialAudioMetadataReader.ReadNextItemCommand, ISpatialAudioMetadataReader::ReadNextItemCommand, ReadNextItemCommand, ReadNextItemCommand method [Core Audio], ReadNextItemCommand method [Core Audio],ISpatialAudioMetadataReader interface, coreaudio.ispatialaudiometadatareader_readnextitemcommand, spatialaudiometadata/ISpatialAudioMetadataReader::ReadNextItemCommand
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
 - ISpatialAudioMetadataReader::ReadNextItemCommand
 - spatialaudiometadata/ISpatialAudioMetadataReader::ReadNextItemCommand
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
 - ISpatialAudioMetadataReader.ReadNextItemCommand
---

# ISpatialAudioMetadataReader::ReadNextItemCommand


## -description

Reads metadata commands and value data for the current item.

## -parameters

### -param commandID [out]

Receives the command ID for the current command.

### -param valueBuffer [in]

A pointer to a buffer which receives data specific to the command as specified by the
metadata format definition. The buffer must be at least <i>maxValueBufferLength</i> to ensure all commands can be successfully retrieved.

### -param maxValueBufferLength [in]

The maximum size of a command value.

### -param valueBufferLength [out]

The size, in bytes, of the data written to the  <i>valueBuffer</i> parameter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the provided pointers is not valid.

</td>
</tr>
</table>

## -remarks

Before calling <b>ReadNextItem</b>, you must open the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a> for reading by calling <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open">Open</a> after the object is created and after <a href="/windows/desktop/CoreAudio/ispatialaudiometadatawriter-close">Close</a> has been called. You must also call <a href="/previous-versions/windows/desktop/legacy/mt798194(v=vs.85)">ReadItemCountInFrames</a> and then call <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-readnextitem">ReadNextItem</a> before calling <b>ReadNextItem</b>.

The <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a> keeps an internal pointer to the current position within the total range of frames contained by the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> with which the reader is associated. Each call to this method causes the pointer to be advanced by the number of frames specified in the <i>readFrameCount</i> parameter.

The process for reading commands and the associated values is recursive. After each call to <b>ReadItemCountInFrames</b>, call <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-readnextitem">ReadNextItem</a> to get the number of commands in the next item. After every call to <b>ReadNextItem</b>, call <b>ReadNextItemCommand</b> to read each command for the  item. Repeat this process until the entire frame range of the <b>ISpatialAudioMetadataItems</b> has been read.

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>