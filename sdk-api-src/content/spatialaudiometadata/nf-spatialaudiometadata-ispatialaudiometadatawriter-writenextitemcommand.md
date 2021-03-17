---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataWriter.WriteNextItemCommand
title: ISpatialAudioMetadataWriter::WriteNextItemCommand (spatialaudiometadata.h)
description: Writes metadata commands and value data to the current item.
helpviewer_keywords: ["ISpatialAudioMetadataWriter interface [Core Audio]","WriteNextItemCommand method","ISpatialAudioMetadataWriter.WriteNextItemCommand","ISpatialAudioMetadataWriter::WriteNextItemCommand","WriteNextItemCommand","WriteNextItemCommand method [Core Audio]","WriteNextItemCommand method [Core Audio]","ISpatialAudioMetadataWriter interface","coreaudio.ispatialaudiometadatawriter_writenextitemcommand","spatialaudiometadata/ISpatialAudioMetadataWriter::WriteNextItemCommand"]
old-location: coreaudio\ispatialaudiometadatawriter_writenextitemcommand.htm
tech.root: CoreAudio
ms.assetid: A614AEC6-7CA3-4624-BAFE-46618BCB64FA
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataWriter interface [Core Audio],WriteNextItemCommand method, ISpatialAudioMetadataWriter.WriteNextItemCommand, ISpatialAudioMetadataWriter::WriteNextItemCommand, WriteNextItemCommand, WriteNextItemCommand method [Core Audio], WriteNextItemCommand method [Core Audio],ISpatialAudioMetadataWriter interface, coreaudio.ispatialaudiometadatawriter_writenextitemcommand, spatialaudiometadata/ISpatialAudioMetadataWriter::WriteNextItemCommand
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
 - ISpatialAudioMetadataWriter::WriteNextItemCommand
 - spatialaudiometadata/ISpatialAudioMetadataWriter::WriteNextItemCommand
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
 - ISpatialAudioMetadataWriter.WriteNextItemCommand
---

# ISpatialAudioMetadataWriter::WriteNextItemCommand


## -description

Writes metadata commands and value data to the current item.

## -parameters

### -param commandID [in]

A command supported by the metadata format of the  object.  The call will fail if the command not defined by metadata format. Each command can
only be written once per item.

### -param valueBuffer [in]

A pointer to a buffer which stores data specific to the command as specified by the
metadata format definition.

### -param valueBufferLength [in]

The size, in bytes, of the command data supplied in the  <i>valueBuffer</i> parameter.  The size must match command definition specified by the metadata format or the call will fail.

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
The <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> has not been opened for writing with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open">Open</a> or the object has been closed for writing with a call to <a href="/windows/desktop/CoreAudio/ispatialaudiometadatawriter-close">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_ITEMOFFSET_WRITTEN</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-writenextitem">WriteNextItem</a> was not called after <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open">Open</a> was called and before the call to <b>WriteNextItemCommand</b>.

</td>
</tr>
</table>

## -remarks

You must open the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> for writing by calling <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open">Open</a>, and set the current metadata item offset by calling <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-writenextitem">WriteNextItem</a> before calling <b>WriteNextItemCommand</b>.

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>