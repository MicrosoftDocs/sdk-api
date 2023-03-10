---
UID: NN:indexsrv.IStemmer
title: IStemmer (indexsrv.h)
description: Provides methods for creating a language-specific stemmer. The stemmer generates inflected forms of a specified word.
helpviewer_keywords: ["IStemmer","IStemmer interface [search]","IStemmer interface [search]","described","_search_IStemmer","indexsrv/IStemmer","search._search_IStemmer"]
old-location: search\_search_IStemmer.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\istemmer\istemmer.htm
ms.date: 12/05/2018
ms.keywords: IStemmer, IStemmer interface [search], IStemmer interface [search],described, _search_IStemmer, indexsrv/IStemmer, search._search_IStemmer
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
req.redist: Windows NT 4.0 Option Pack
ms.custom: 19H1
f1_keywords:
 - IStemmer
 - indexsrv/IStemmer
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
 - IStemmer
---

# IStemmer interface


## -description

Provides methods for creating a language-specific stemmer. The stemmer generates inflected forms of a specified word.

## -inheritance

The <b>IStemmer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStemmer</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface to create a custom stemmer for a language. Windows Search calls the methods of this interface to generate inflected forms for words identified when building an index.

Stemmer components for Windows Search run in the Local Security context. They should be written to manage buffers and the stack correctly. All string copies must have explicit checks to guard against buffer overruns. You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.
