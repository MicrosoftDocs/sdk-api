---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataWriter.WriteNextItem
title: ISpatialAudioMetadataWriter::WriteNextItem (spatialaudiometadata.h)
description: Starts a new metadata item at the specified offset.
helpviewer_keywords: ["ISpatialAudioMetadataWriter interface [Core Audio]","WriteNextItem method","ISpatialAudioMetadataWriter.WriteNextItem","ISpatialAudioMetadataWriter::WriteNextItem","WriteNextItem","WriteNextItem method [Core Audio]","WriteNextItem method [Core Audio]","ISpatialAudioMetadataWriter interface","coreaudio.ispatialaudiometadatawriter_writenextitem","spatialaudiometadata/ISpatialAudioMetadataWriter::WriteNextItem"]
old-location: coreaudio\ispatialaudiometadatawriter_writenextitem.htm
tech.root: CoreAudio
ms.assetid: 9D61BFC0-BAD7-46D3-B0E9-4848E37785E9
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataWriter interface [Core Audio],WriteNextItem method, ISpatialAudioMetadataWriter.WriteNextItem, ISpatialAudioMetadataWriter::WriteNextItem, WriteNextItem, WriteNextItem method [Core Audio], WriteNextItem method [Core Audio],ISpatialAudioMetadataWriter interface, coreaudio.ispatialaudiometadatawriter_writenextitem, spatialaudiometadata/ISpatialAudioMetadataWriter::WriteNextItem
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
 - ISpatialAudioMetadataWriter::WriteNextItem
 - spatialaudiometadata/ISpatialAudioMetadataWriter::WriteNextItem
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
 - ISpatialAudioMetadataWriter.WriteNextItem
---

# ISpatialAudioMetadataWriter::WriteNextItem


## -description

Starts a new metadata item at the specified offset.

## -parameters

### -param frameOffset [in]

The frame offset of the item within the range specified with the <i>frameCount</i> parameter to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a>.

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
<dt><b>SPTLAUD_MD_CLNT_E_FRAMEOFFSET_OUT_OF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The number of items written in the writing session is greater than the value supplied in the <b>MaxMetadataItemCount</b> field in the <a href="/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParam</a> passed into <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a>. 

The <i>frameCount</i> value is greater than the value of the <i>frameCount</i> parameter to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a> and the overflow mode was set to  <b>SpatialAudioMetadataWriterOverflow_Fail</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>frameOffset</i> is not greater than the value provided  in the previous call to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-writenextitem">WriteNextItem</a> within the same writing session.

</td>
</tr>
</table>

## -remarks

Before calling <b>WriteNextItem</b>, you must open the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> for writing by calling <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open">Open</a> after the object is created and after <a href="/windows/desktop/CoreAudio/ispatialaudiometadatawriter-close">Close</a> has been called. During a writing session demarcated by calls to <b>Open</b> and <b>Close</b>, the value of the <i>frameOffset</i> parameter must be greater than the value in the preceding call.  

Within a single writing session, you must not use <b>WriteNextItem</b> to write more items than the value supplied in the <b>MaxMetadataItemCount</b> field in the <a href="/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParam</a> passed into <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> or an SPTLAUD_MD_CLNT_E_FRAMEOFFSET_OUT_OF_RANGE error will occur. 

If the overflow mode is set to <b>SpatialAudioMetadataWriterOverflow_Fail</b>, the value of the <i>frameOffset</i> parameter must be less than he value of the <i>frameCount</i> parameter to <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a> or an SPTLAUD_MD_CLNT_E_FRAMEOFFSET_OUT_OF_RANGE error will occur.

After calling <b>WriteNextItem</b>, call <a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-writenextitemcommand">WriteNextItemCommand</a> to write metadata commands and value data for the item.

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>