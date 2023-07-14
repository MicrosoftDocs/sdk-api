---
UID: NF:bdatif.IEnumTuneRequests.Skip
title: IEnumTuneRequests::Skip (bdatif.h)
description: The Skip method skips over the specified number of items in the collection.
helpviewer_keywords: ["IEnumTuneRequests interface [Microsoft TV Technologies]","Skip method","IEnumTuneRequests.Skip","IEnumTuneRequests::Skip","IEnumTuneRequestsSkip","Skip","Skip method [Microsoft TV Technologies]","Skip method [Microsoft TV Technologies]","IEnumTuneRequests interface","bdatif/IEnumTuneRequests::Skip","mstv.ienumtunerequests_skip"]
old-location: mstv\ienumtunerequests_skip.htm
tech.root: mstv
ms.assetid: 43ed5c7e-2d31-417e-9d87-c3100e5096d0
ms.date: 12/05/2018
ms.keywords: IEnumTuneRequests interface [Microsoft TV Technologies],Skip method, IEnumTuneRequests.Skip, IEnumTuneRequests::Skip, IEnumTuneRequestsSkip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],IEnumTuneRequests interface, bdatif/IEnumTuneRequests::Skip, mstv.ienumtunerequests_skip
req.header: bdatif.h
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
 - IEnumTuneRequests::Skip
 - bdatif/IEnumTuneRequests::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IEnumTuneRequests.Skip
---

# IEnumTuneRequests::Skip


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Skip</b> method skips over the specified number of items in the collection.

## -parameters

### -param celt [in]

Specifies the number of items to skip.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ienumtunerequests">IEnumTuneRequests Interface</a>