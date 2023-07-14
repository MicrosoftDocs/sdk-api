---
UID: NF:sbe.IEnumStreamBufferRecordingAttrib.Skip
title: IEnumStreamBufferRecordingAttrib::Skip (sbe.h)
description: The Skip method skips over a specified number of attributes.
helpviewer_keywords: ["IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies]","Skip method","IEnumStreamBufferRecordingAttrib.Skip","IEnumStreamBufferRecordingAttrib::Skip","IEnumStreamBufferRecordingAttribSkip","Skip","Skip method [Microsoft TV Technologies]","Skip method [Microsoft TV Technologies]","IEnumStreamBufferRecordingAttrib interface","mstv.ienumstreambufferrecordingattrib_skip","sbe/IEnumStreamBufferRecordingAttrib::Skip"]
old-location: mstv\ienumstreambufferrecordingattrib_skip.htm
tech.root: mstv
ms.assetid: 83beb8e9-f268-4ae1-a90b-548f0e3f6c99
ms.date: 12/05/2018
ms.keywords: IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],Skip method, IEnumStreamBufferRecordingAttrib.Skip, IEnumStreamBufferRecordingAttrib::Skip, IEnumStreamBufferRecordingAttribSkip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],IEnumStreamBufferRecordingAttrib interface, mstv.ienumstreambufferrecordingattrib_skip, sbe/IEnumStreamBufferRecordingAttrib::Skip
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IEnumStreamBufferRecordingAttrib::Skip
 - sbe/IEnumStreamBufferRecordingAttrib::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IEnumStreamBufferRecordingAttrib.Skip
---

# IEnumStreamBufferRecordingAttrib::Skip


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Skip</b> method skips over a specified number of attributes.

## -parameters

### -param cRecords [in]

The number of attributes to skip.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped past the end of the sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-ienumstreambufferrecordingattrib">IEnumStreamBufferRecordingAttrib Interface</a>