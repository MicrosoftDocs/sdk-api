---
UID: NF:bdatif.IEnumTuneRequests.Clone
title: IEnumTuneRequests::Clone (bdatif.h)
description: The Clone method creates a copy of the collection.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","IEnumTuneRequests interface","IEnumTuneRequests interface [Microsoft TV Technologies]","Clone method","IEnumTuneRequests.Clone","IEnumTuneRequests::Clone","IEnumTuneRequestsClone","bdatif/IEnumTuneRequests::Clone","mstv.ienumtunerequests_clone"]
old-location: mstv\ienumtunerequests_clone.htm
tech.root: mstv
ms.assetid: 9910d646-c98e-479a-8abd-5d5427ef11b5
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IEnumTuneRequests interface, IEnumTuneRequests interface [Microsoft TV Technologies],Clone method, IEnumTuneRequests.Clone, IEnumTuneRequests::Clone, IEnumTuneRequestsClone, bdatif/IEnumTuneRequests::Clone, mstv.ienumtunerequests_clone
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
 - IEnumTuneRequests::Clone
 - bdatif/IEnumTuneRequests::Clone
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
 - IEnumTuneRequests.Clone
---

# IEnumTuneRequests::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method creates a copy of the collection.

## -parameters

### -param ppenum [out]

Receives the new collection.

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