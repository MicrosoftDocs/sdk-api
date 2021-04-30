---
UID: NF:textstor.ITextStoreACP.GetEndACP
title: ITextStoreACP::GetEndACP (textstor.h)
description: The ITextStoreACP::GetEndACP method returns the number of characters in a document.
helpviewer_keywords: ["GetEndACP","GetEndACP method [Text Services Framework]","GetEndACP method [Text Services Framework]","ITextStoreACP interface","ITextStoreACP interface [Text Services Framework]","GetEndACP method","ITextStoreACP.GetEndACP","ITextStoreACP::GetEndACP","_tsf_itextstoreacp_getendacp_ref","textstor/ITextStoreACP::GetEndACP","tsf.itextstoreacp_getendacp"]
old-location: tsf\itextstoreacp_getendacp.htm
tech.root: TSF
ms.assetid: 741ec23f-9d73-40ee-af94-f9a18bbb8e87
ms.date: 12/05/2018
ms.keywords: GetEndACP, GetEndACP method [Text Services Framework], GetEndACP method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetEndACP method, ITextStoreACP.GetEndACP, ITextStoreACP::GetEndACP, _tsf_itextstoreacp_getendacp_ref, textstor/ITextStoreACP::GetEndACP, tsf.itextstoreacp_getendacp
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP::GetEndACP
 - textstor/ITextStoreACP::GetEndACP
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
 - ITextStoreACP.GetEndACP
---

# ITextStoreACP::GetEndACP


## -description

The <b>ITextStoreACP::GetEndACP</b> method returns the number of characters in a document.

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
The application has not implemented this method. This is usually an indication that calculating the end position requires excessive resources. If the end position is necessary, you can use <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext">ITextStoreACP::GetText</a> to calculate it, though this can also be a memory-intensive operation, paging in arbitrarily large amounts of memory from disk.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext">ITextStoreACP::GetText
      </a>