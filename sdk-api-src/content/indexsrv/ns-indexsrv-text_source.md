---
UID: NS:indexsrv.tagTEXT_SOURCE
title: TEXT_SOURCE (indexsrv.h)
description: Contains information about text that the word breaker will process.
helpviewer_keywords: ["TEXT_SOURCE","TEXT_SOURCE structure [search]","_search_TEXT_SOURCE","indexsrv/TEXT_SOURCE","search._search_TEXT_SOURCE","tagTEXT_SOURCE"]
old-location: search\_search_TEXT_SOURCE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\text_source.htm
ms.date: 12/05/2018
ms.keywords: TEXT_SOURCE, TEXT_SOURCE structure [search], _search_TEXT_SOURCE, indexsrv/TEXT_SOURCE, search._search_TEXT_SOURCE, tagTEXT_SOURCE
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
req.typenames: TEXT_SOURCE
req.redist: the Windows NT 4.0 Option Pack
ms.custom: 19H1
f1_keywords:
 - tagTEXT_SOURCE
 - indexsrv/tagTEXT_SOURCE
 - TEXT_SOURCE
 - indexsrv/TEXT_SOURCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Indexsrv.h
api_name:
 - TEXT_SOURCE
---

# TEXT_SOURCE structure


## -description

Contains information about text that the word breaker will process.

## -struct-fields

### -field pfnFillTextBuffer

Type: <b>PFNFILLTEXTBUFFER</b>

Pointer to a function, <b>PFNFILLTEXTBUFFER</b> that refills the <b>awcBuffer</b> with text from the source document.

### -field awcBuffer

Type: <b>WCHAR*</b>

Pointer to a buffer that contains text from the source document for the word breaker to parse.

### -field iEnd

Type: <b>ULONG</b>

Position of the last character in <b>awcBuffer</b>.

### -field iCur

Type: <b>ULONG</b>

Position of the first character in <b>awcBuffer</b>.

## -remarks

Windows Search populates the members of this structure when the word breaker is invoked and initialized. <a href="/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext">IWordBreaker::BreakText</a> gets a pointer to a <b>TEXT_SOURCE</b> structure and calls PFNFILLTEXTBUFFER, the function pointed to by the <b>pfnFillTextBuffer</b> member, to refill <b>awcBuffer</b> until all text from the source is processed. The <b>PFNFILLTEXTBUFFER</b> function returns an <b>HRESULT</b> that includes both filtering and word-breaking return values.

The filtering return values are the following:

<ul>
<li>FILTER_E_NO_MORE_VALUES</li>
<li>FILTER_E_NO_TEXT</li>
<li>FILTER_E_NO_VALUES</li>
<li>FILTER_E_NO_MORE_TEXT</li>
<li>FILTER_E_END_OF_CHUNKS</li>
</ul>
For more information about these return values, see <a href="/previous-versions/windows/desktop/indexsrv/filter-interface-values">Filter-Interface Values</a>.

The word-breaking return value is WBREAK_E_END_OF_TEXT. For more information about word-breaking return values, see <a href="/previous-versions/windows/desktop/indexsrv/word-breaking-values">Word-Breaking Values</a>.

## -see-also

<a href="/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext">IWordBreaker::BreakText</a>