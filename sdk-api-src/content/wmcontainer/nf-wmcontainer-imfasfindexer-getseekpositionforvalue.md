---
UID: NF:wmcontainer.IMFASFIndexer.GetSeekPositionForValue
title: IMFASFIndexer::GetSeekPositionForValue (wmcontainer.h)
description: Given a desired seek time, gets the offset from which the client should start reading data.
helpviewer_keywords: ["GetSeekPositionForValue","GetSeekPositionForValue method [Media Foundation]","GetSeekPositionForValue method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GetSeekPositionForValue method","IMFASFIndexer.GetSeekPositionForValue","IMFASFIndexer::GetSeekPositionForValue","c8e9982e-b056-48dc-ac5f-20bf65b475ec","mf.imfasfindexer_getseekpositionforvalue","wmcontainer/IMFASFIndexer::GetSeekPositionForValue"]
old-location: mf\imfasfindexer_getseekpositionforvalue.htm
tech.root: mf
ms.assetid: c8e9982e-b056-48dc-ac5f-20bf65b475ec
ms.date: 12/05/2018
ms.keywords: GetSeekPositionForValue, GetSeekPositionForValue method [Media Foundation], GetSeekPositionForValue method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetSeekPositionForValue method, IMFASFIndexer.GetSeekPositionForValue, IMFASFIndexer::GetSeekPositionForValue, c8e9982e-b056-48dc-ac5f-20bf65b475ec, mf.imfasfindexer_getseekpositionforvalue, wmcontainer/IMFASFIndexer::GetSeekPositionForValue
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFIndexer::GetSeekPositionForValue
 - wmcontainer/IMFASFIndexer::GetSeekPositionForValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFIndexer.GetSeekPositionForValue
---

# IMFASFIndexer::GetSeekPositionForValue


## -description

Given a desired seek time, gets the offset from which the client should start reading data.

## -parameters

### -param pvarValue [in]

The value of the index entry for which to get the position. The format of this value varies depending on the type of index, which is specified in the index identifier. For time-based indexing, the variant type is <b>VT_I8</b> and the value is the desired seek time, in 100-nanosecond units.

### -param pIndexIdentifier [in]

Pointer to an <a href="/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier">ASF_INDEX_IDENTIFIER</a> structure that identifies the stream number and index type.

### -param pcbOffsetWithinData [out]

Receives the offset within the data segment of the ASF Data Object. The offset is in bytes, and is relative to the start of packet 0. The offset gives the starting location from which the client should begin reading from the stream. This location might not correspond exactly to the requested seek time.
          

For reverse playback, if no key frame exists after the desired seek position, this parameter receives the value <b>MFASFINDEXER_READ_FOR_REVERSEPLAYBACK_OUTOFDATASEGMENT</b>. In that case, the seek position should be 1 byte pass the end of the data segment.

### -param phnsApproxTime [out]

Receives the approximate time stamp of the data that is located at the offset returned in the <i>pcbOffsetWithinData</i> parameter. The accuracy of this value is equal to the indexing interval of the ASF index, typically about 1 second.
          

<ul>
<li>If the index type specified in <i>pIndexIdentifier</i> is <b>GUID_NULL</b> (time indexing), this parameter can be <b>NULL</b>.
              </li>
<li>For all other index types, this parameter must be <b>NULL</b>.
              </li>
</ul>
If the approximate time stamp cannot be determined, this parameter receives the value <b>MFASFINDEXER_APPROX_SEEK_TIME_UNKNOWN</b>.

### -param pdwPayloadNumberOfStreamWithinPacket [out]

Receives the payload number of the payload that contains the information for the specified stream. Packets can contain multiple payloads, each containing data for a different stream. This parameter can be <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ASF_OUTOFRANGE</b></dt>
</dl>
</td>
<td width="60%">
The requested seek time is out of range.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_INDEX</b></dt>
</dl>
</td>
<td width="60%">
No index exists of the specified type for the specified stream.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>