---
UID: NE:indexsrv.tagWORDREP_BREAK_TYPE
title: WORDREP_BREAK_TYPE (indexsrv.h)
description: Describes the type of break that separates the current word from the previous word.
helpviewer_keywords: ["WORDREP_BREAK_EOC","WORDREP_BREAK_EOP","WORDREP_BREAK_EOS","WORDREP_BREAK_EOW","WORDREP_BREAK_TYPE","WORDREP_BREAK_TYPE enumeration [Indexing Service]","_idxs_WORDREP_BREAK_TYPE","indexsrv.wordrep_break_type","indexsrv/WORDREP_BREAK_EOC","indexsrv/WORDREP_BREAK_EOP","indexsrv/WORDREP_BREAK_EOS","indexsrv/WORDREP_BREAK_EOW","indexsrv/WORDREP_BREAK_TYPE"]
old-location: indexsrv\wordrep_break_type.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_12at.htm
ms.date: 12/05/2018
ms.keywords: WORDREP_BREAK_EOC, WORDREP_BREAK_EOP, WORDREP_BREAK_EOS, WORDREP_BREAK_EOW, WORDREP_BREAK_TYPE, WORDREP_BREAK_TYPE enumeration [Indexing Service], _idxs_WORDREP_BREAK_TYPE, indexsrv.wordrep_break_type, indexsrv/WORDREP_BREAK_EOC, indexsrv/WORDREP_BREAK_EOP, indexsrv/WORDREP_BREAK_EOS, indexsrv/WORDREP_BREAK_EOW, indexsrv/WORDREP_BREAK_TYPE
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
req.typenames: WORDREP_BREAK_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWORDREP_BREAK_TYPE
 - indexsrv/tagWORDREP_BREAK_TYPE
 - WORDREP_BREAK_TYPE
 - indexsrv/WORDREP_BREAK_TYPE
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
 - WORDREP_BREAK_TYPE
---

# WORDREP_BREAK_TYPE enumeration


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Describes the type of break that separates the current word from the previous word.

## -enum-fields

### -field WORDREP_BREAK_EOW:0

A word break is placed between this word and the previous word that was placed in the <b>WordSink</b>. This break is the default used by the <a href="/windows/desktop/search/iwordsink-putword">PutWord</a> method.

### -field WORDREP_BREAK_EOS:1

A sentence break is placed between this word and the previous word.

### -field WORDREP_BREAK_EOP:2

A paragraph break is placed between this word and the previous word.

### -field WORDREP_BREAK_EOC:3

A chapter break is placed between this word and the previous word.

## -see-also

<a href="/windows/desktop/search/iwordsink-putaltword">IWordSink::PutAltWord</a>



<a href="/windows/desktop/search/iwordsink-putword">IWordSink::PutWord</a>
