---
UID: NF:bdatif.IEnumTuneRequests.Next
title: IEnumTuneRequests::Next (bdatif.h)
description: The Next method retrieves the specified number of items in the collection.
helpviewer_keywords: ["IEnumTuneRequests interface [Microsoft TV Technologies]","Next method","IEnumTuneRequests.Next","IEnumTuneRequests::Next","IEnumTuneRequestsNext","Next","Next method [Microsoft TV Technologies]","Next method [Microsoft TV Technologies]","IEnumTuneRequests interface","bdatif/IEnumTuneRequests::Next","mstv.ienumtunerequests_next"]
old-location: mstv\ienumtunerequests_next.htm
tech.root: mstv
ms.assetid: fb846bdb-f0ce-44f7-8d15-608c21e095c1
ms.date: 12/05/2018
ms.keywords: IEnumTuneRequests interface [Microsoft TV Technologies],Next method, IEnumTuneRequests.Next, IEnumTuneRequests::Next, IEnumTuneRequestsNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumTuneRequests interface, bdatif/IEnumTuneRequests::Next, mstv.ienumtunerequests_next
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
 - IEnumTuneRequests::Next
 - bdatif/IEnumTuneRequests::Next
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
 - IEnumTuneRequests.Next
---

# IEnumTuneRequests::Next


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Next</b> method retrieves the specified number of items in the collection.

## -parameters

### -param celt [in]

Specifies the number of items to retrieve.

### -param ppprop [out]

Array of size <i>celt</i> that is filled with <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface pointers.

### -param pcelt [out]

Receives the number of items retrieved.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The collection is at the end of the enumeration sequence.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ienumtunerequests">IEnumTuneRequests Interface</a>