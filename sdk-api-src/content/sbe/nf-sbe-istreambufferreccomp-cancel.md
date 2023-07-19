---
UID: NF:sbe.IStreamBufferRecComp.Cancel
title: IStreamBufferRecComp::Cancel (sbe.h)
description: The Cancel method cancels an append operation, if one is in progress. Otherwise, it has no effect.
helpviewer_keywords: ["Cancel","Cancel method [Microsoft TV Technologies]","Cancel method [Microsoft TV Technologies]","IStreamBufferRecComp interface","IStreamBufferRecComp interface [Microsoft TV Technologies]","Cancel method","IStreamBufferRecComp.Cancel","IStreamBufferRecComp::Cancel","IStreamBufferRecCompCancel","mstv.istreambufferreccomp_cancel","sbe/IStreamBufferRecComp::Cancel"]
old-location: mstv\istreambufferreccomp_cancel.htm
tech.root: mstv
ms.assetid: d7355f5d-034c-404f-b6c7-02c04c87285d
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Microsoft TV Technologies], Cancel method [Microsoft TV Technologies],IStreamBufferRecComp interface, IStreamBufferRecComp interface [Microsoft TV Technologies],Cancel method, IStreamBufferRecComp.Cancel, IStreamBufferRecComp::Cancel, IStreamBufferRecCompCancel, mstv.istreambufferreccomp_cancel, sbe/IStreamBufferRecComp::Cancel
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
 - IStreamBufferRecComp::Cancel
 - sbe/IStreamBufferRecComp::Cancel
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
 - IStreamBufferRecComp.Cancel
---

# IStreamBufferRecComp::Cancel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Cancel</b> method cancels an append operation, if one is in progress. Otherwise, it has no effect.



## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
Success

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferreccomp">IStreamBufferRecComp Interface</a>
