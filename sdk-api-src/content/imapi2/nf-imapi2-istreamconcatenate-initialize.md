---
UID: NF:imapi2.IStreamConcatenate.Initialize
title: IStreamConcatenate::Initialize (imapi2.h)
description: Initializes this stream from two input streams.
helpviewer_keywords: ["IStreamConcatenate interface [IMAPI]","Initialize method","IStreamConcatenate.Initialize","IStreamConcatenate::Initialize","Initialize","Initialize method [IMAPI]","Initialize method [IMAPI]","IStreamConcatenate interface","imapi.istreamconcatenate_initialize","imapi2/IStreamConcatenate::Initialize"]
old-location: imapi\istreamconcatenate_initialize.htm
tech.root: imapi
ms.assetid: 62db148e-926d-47b3-a0f6-945730177184
ms.date: 12/05/2018
ms.keywords: IStreamConcatenate interface [IMAPI],Initialize method, IStreamConcatenate.Initialize, IStreamConcatenate::Initialize, Initialize, Initialize method [IMAPI], Initialize method [IMAPI],IStreamConcatenate interface, imapi.istreamconcatenate_initialize, imapi2/IStreamConcatenate::Initialize
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IStreamConcatenate::Initialize
 - imapi2/IStreamConcatenate::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IStreamConcatenate.Initialize
---

# IStreamConcatenate::Initialize


## -description

Initializes this stream from two input streams.

## -parameters

### -param stream1 [in]

An <b>IStream</b> interface of the first stream to add to this stream.

### -param stream2 [in]

An <b>IStream</b> interface of the second stream to add to this stream.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
</table>

## -remarks

When using the <a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate">IStreamConcatenate</a> interface, the following  scenarios will result in undefined behaviors, and should be avoided:

<ul>
<li>Each partial stream composing the MsftStreamConcatenate object is actually the same stream.</li>
<li>Any of the concatenated streams are modified (read from, written to, or seeked on) outside of IMAPI.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate">IStreamConcatenate</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreamconcatenate-initialize2">IStreamConcatenate::Initialize2</a>