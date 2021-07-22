---
UID: NN:indexsrv.IPhraseSink
title: IPhraseSink (indexsrv.h)
description: Handles phrases that word breakers parse from query text during query time.
helpviewer_keywords: ["IPhraseSink","IPhraseSink interface [Indexing Service]","IPhraseSink interface [Indexing Service]","described","_idxs_PhraseSink","indexsrv.iphrasesink","indexsrv/IPhraseSink"]
old-location: indexsrv\iphrasesink.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_3asr.htm
ms.date: 12/05/2018
ms.keywords: IPhraseSink, IPhraseSink interface [Indexing Service], IPhraseSink interface [Indexing Service],described, _idxs_PhraseSink, indexsrv.iphrasesink, indexsrv/IPhraseSink
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
 - IPhraseSink
 - indexsrv/IPhraseSink
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
 - IPhraseSink
 - IPhraseSink.PutSmallPhrase
---

# IPhraseSink interface


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Handles phrases that word breakers parse from query text during query time.

## -inheritance

The <b>IPhraseSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhraseSink</b> also has these types of members:

## -remarks

Indexing Service creates and initializes instances of the PhraseSink object. The PhraseSink receives the <i>fQuery</i> parameter during initialization and uses this parameter to determine the word-breaking context in which the object is being used.




<a href="/windows/desktop/api/indexsrv/nn-indexsrv-iwordbreaker">IWordBreaker</a> implementations receive a pointer to the PhraseSink object in the <a href="/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext">BreakText</a> method.

## -see-also

<a href="/windows/desktop/api/indexsrv/nn-indexsrv-iwordbreaker">IWordBreaker</a>
