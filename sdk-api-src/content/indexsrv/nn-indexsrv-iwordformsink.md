---
UID: NN:indexsrv.IWordFormSink
title: IWordFormSink (indexsrv.h)
description: Handles the list of alternative word forms that stemmers generate during query time.
helpviewer_keywords: ["IWordFormSink","IWordFormSink interface [search]","IWordFormSink interface [search]","described","indexsrv/IWordFormSink","search.iwordformsink"]
old-location: search\iwordformsink.htm
tech.root: search
ms.assetid: 81D52B0C-BADD-48C0-85DB-57CA82D7BBA8
ms.date: 12/05/2018
ms.keywords: IWordFormSink, IWordFormSink interface [search], IWordFormSink interface [search],described, indexsrv/IWordFormSink, search.iwordformsink
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
 - IWordFormSink
 - indexsrv/IWordFormSink
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
 - IWordFormSink
---

# IWordFormSink interface


## -description

Handles the list of alternative word forms that stemmers generate during query time.

## -inheritance

The <b>IWordFormSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWordFormSink</b> also has these types of members:

## -remarks

Windows Search creates and initializes instances of the StemSink object. The <b>IWordFormSink</b> object receives the <i>ulMaxTokenSize</i> parameter during initialization. The value for this parameter is determined by the <a href="/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a> implementation and determines the maximum length, in characters, for a single word that the <b>IWordFormSink</b> handles.




<a href="/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a> implementations receive a pointer to the <b>IWordFormSink</b> object in the <a href="/windows/desktop/api/indexsrv/nf-indexsrv-istemmer-generatewordforms">GenerateWordForms</a> method.

## -see-also

<a href="/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a>
