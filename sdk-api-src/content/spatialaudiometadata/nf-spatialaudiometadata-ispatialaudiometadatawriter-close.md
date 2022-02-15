---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataWriter.Close
title: ISpatialAudioMetadataWriter::Close (spatialaudiometadata.h)
description: Completes any needed operations on the metadata buffer and releases the specified ISpatialAudioMetadataItems object.
helpviewer_keywords: ["Close","Close method [Core Audio]","Close method [Core Audio]","ISpatialAudioMetadataWriter interface","ISpatialAudioMetadataWriter interface [Core Audio]","Close method","ISpatialAudioMetadataWriter.Close","ISpatialAudioMetadataWriter::Close","coreaudio.ispatialaudiometadatawriter_close","spatialaudiometadata/ISpatialAudioMetadataWriter::Close"]
old-location: coreaudio\ispatialaudiometadatawriter_close.htm
tech.root: CoreAudio
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
ms.date: 12/05/2018
ms.keywords: Close, Close method [Core Audio], Close method [Core Audio],ISpatialAudioMetadataWriter interface, ISpatialAudioMetadataWriter interface [Core Audio],Close method, ISpatialAudioMetadataWriter.Close, ISpatialAudioMetadataWriter::Close, coreaudio.ispatialaudiometadatawriter_close, spatialaudiometadata/ISpatialAudioMetadataWriter::Close
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
 - ISpatialAudioMetadataWriter::Close
 - spatialaudiometadata/ISpatialAudioMetadataWriter::Close
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
 - ISpatialAudioMetadataWriter.Close
---

# ISpatialAudioMetadataWriter::Close


## -description

Completes any needed operations on the metadata buffer and releases the specified <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object.



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
The supplied <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> has not been opened with a call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open">Open</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_ITEMS_WRITTEN</b></dt>
</dl>
</td>
<td width="60%">
No metadata items have been written to the supplied <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_ITEM_MUST_HAVE_COMMANDS</b></dt>
</dl>
</td>
<td width="60%">
No metadata commands have been written to the supplied <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>
