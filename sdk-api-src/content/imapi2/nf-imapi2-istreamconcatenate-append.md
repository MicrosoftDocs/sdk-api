---
UID: NF:imapi2.IStreamConcatenate.Append
title: IStreamConcatenate::Append (imapi2.h)
description: Appends a stream to this stream.
helpviewer_keywords: ["Append","Append method [IMAPI]","Append method [IMAPI]","IStreamConcatenate interface","IStreamConcatenate interface [IMAPI]","Append method","IStreamConcatenate.Append","IStreamConcatenate::Append","imapi.istreamconcatenate_append","imapi2/IStreamConcatenate::Append"]
old-location: imapi\istreamconcatenate_append.htm
tech.root: imapi
ms.assetid: 9871cc35-c955-4fd4-9082-5b6ab60cae7b
ms.date: 12/05/2018
ms.keywords: Append, Append method [IMAPI], Append method [IMAPI],IStreamConcatenate interface, IStreamConcatenate interface [IMAPI],Append method, IStreamConcatenate.Append, IStreamConcatenate::Append, imapi.istreamconcatenate_append, imapi2/IStreamConcatenate::Append
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
 - IStreamConcatenate::Append
 - imapi2/IStreamConcatenate::Append
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
 - IStreamConcatenate.Append
---

# IStreamConcatenate::Append


## -description

Appends a stream to this stream.

## -parameters

### -param stream [in]

An <b>IStream</b> interface of the stream to append to this stream.

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

To append more than one stream to this stream, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-istreamconcatenate-append2">IStreamConcatenate::Append2</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate">IStreamConcatenate</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-istreamconcatenate-append2">IStreamConcatenate::Append2</a>