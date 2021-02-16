---
UID: NF:textstor.ITextStoreACP2.GetEndACP
title: ITextStoreACP2::GetEndACP (textstor.h)
description: Gets the number of characters in a document.
helpviewer_keywords: ["GetEndACP","GetEndACP method [Text Services Framework]","GetEndACP method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","GetEndACP method","ITextStoreACP2.GetEndACP","ITextStoreACP2::GetEndACP","textstor/ITextStoreACP2::GetEndACP","tsf.itextstoreacp2_getendacp"]
old-location: tsf\itextstoreacp2_getendacp.htm
tech.root: TSF
ms.assetid: 61429956-8996-450e-af24-0c91ea974865
ms.date: 12/05/2018
ms.keywords: GetEndACP, GetEndACP method [Text Services Framework], GetEndACP method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetEndACP method, ITextStoreACP2.GetEndACP, ITextStoreACP2::GetEndACP, textstor/ITextStoreACP2::GetEndACP, tsf.itextstoreacp2_getendacp
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::GetEndACP
 - textstor/ITextStoreACP2::GetEndACP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.GetEndACP
---

# ITextStoreACP2::GetEndACP


## -description

Gets the number of characters in a document.

## -parameters

### -param pacp [out]

Receives the character position of the last character in the document plus one.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application has not implemented this method. This is usually an indication that calculating the end position requires excessive resources. If the end position is necessary, you can use <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-gettext">GetText</a> to calculate it, though this can also be a memory-intensive operation, paging in arbitrarily large amounts of memory from disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-gettext">GetText</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>