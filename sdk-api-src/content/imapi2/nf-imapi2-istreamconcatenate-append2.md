---
UID: NF:imapi2.IStreamConcatenate.Append2
title: IStreamConcatenate::Append2 (imapi2.h)
description: Appends an array of streams to this stream.
helpviewer_keywords: ["Append2","Append2 method [IMAPI]","Append2 method [IMAPI]","IStreamConcatenate interface","IStreamConcatenate interface [IMAPI]","Append2 method","IStreamConcatenate.Append2","IStreamConcatenate::Append2","imapi.istreamconcatenate_append2","imapi2/IStreamConcatenate::Append2"]
old-location: imapi\istreamconcatenate_append2.htm
tech.root: imapi
ms.assetid: 75e7f4cd-f3c8-494d-b049-7fe32c486659
ms.date: 12/05/2018
ms.keywords: Append2, Append2 method [IMAPI], Append2 method [IMAPI],IStreamConcatenate interface, IStreamConcatenate interface [IMAPI],Append2 method, IStreamConcatenate.Append2, IStreamConcatenate::Append2, imapi.istreamconcatenate_append2, imapi2/IStreamConcatenate::Append2
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
 - IStreamConcatenate::Append2
 - imapi2/IStreamConcatenate::Append2
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
 - IStreamConcatenate.Append2
---

# IStreamConcatenate::Append2


## -description

Appends an array of streams to this stream.

## -parameters

### -param streams [in]

Array of  <b>IStream</b> interfaces of the streams to append to this stream.

### -param streamCount [in]

Number of streams in <i>streams</i>.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>

## -remarks

You must call the <a href="/windows/desktop/api/imapi2/nf-imapi2-istreamconcatenate-initialize">IStreamConcatenate::Initialize</a> or <a href="/windows/desktop/api/imapi2/nf-imapi2-istreamconcatenate-initialize2">IStreamConcatenate::Initialize2</a> method prior to calling this method.

To append a single stream to this stream, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-istreamconcatenate-append">IStreamConcatenate::Append</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate">IStreamConcatenate</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreamconcatenate-append">IStreamConcatenate::Append</a>