---
UID: NF:indexsrv.IPhraseSink.PutPhrase
title: IPhraseSink::PutPhrase (indexsrv.h)
description: Puts a query-time phrase in the IPhraseSink object.
helpviewer_keywords: ["IPhraseSink interface [search]","PutPhrase method","IPhraseSink.PutPhrase","IPhraseSink::PutPhrase","PutPhrase","PutPhrase method [search]","PutPhrase method [search]","IPhraseSink interface","indexsrv/IPhraseSink::PutPhrase","search.iphrasesink_putphrase"]
old-location: search\iphrasesink_putphrase.htm
tech.root: search
ms.assetid: 5E1762A8-8CC9-4EAE-BC79-91672994C1E3
ms.date: 12/05/2018
ms.keywords: IPhraseSink interface [search],PutPhrase method, IPhraseSink.PutPhrase, IPhraseSink::PutPhrase, PutPhrase, PutPhrase method [search], PutPhrase method [search],IPhraseSink interface, indexsrv/IPhraseSink::PutPhrase, search.iphrasesink_putphrase
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IPhraseSink::PutPhrase
 - indexsrv/IPhraseSink::PutPhrase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Indexsrv.h
api_name:
 - IPhraseSink.PutPhrase
---

# IPhraseSink::PutPhrase


## -description

Puts a query-time phrase in the <a href="/windows/desktop/api/indexsrv/nn-indexsrv-iphrasesink">IPhraseSink</a> object.

## -parameters

### -param pwcPhrase [in]

A pointer to a buffer that contains a phrase.

### -param cwcPhrase [in]

The number of characters in <i>pwcPhrase</i>. There is no limit on the size of a query-time phrase.

## -returns

This method can return one of these values.

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
The operation was completed successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PSINK_E_QUERY_ONLY </b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/indexsrv/nf-indexsrv-iphrasesink-putphrase">PutPhrase</a> was called at index time instead of query time.

</td>
</tr>
</table>

## -remarks

<b>PutPhrase</b> is called by the <a href="/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext">IWordBreaker::BreakText</a> method of the <a href="/windows/desktop/api/indexsrv/nn-indexsrv-iwordbreaker">IWordBreaker</a> implementation. Phrases that the <a href="/windows/desktop/api/indexsrv/nn-indexsrv-iphrasesink">IPhraseSink</a> object handles are used by Windows Search to expand the original query text.

## -see-also

<a href="/windows/desktop/api/indexsrv/nn-indexsrv-iphrasesink">IPhraseSink</a>