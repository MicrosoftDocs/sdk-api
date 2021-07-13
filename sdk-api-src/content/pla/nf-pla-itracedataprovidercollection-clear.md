---
UID: NF:pla.ITraceDataProviderCollection.Clear
title: ITraceDataProviderCollection::Clear (pla.h)
description: Removes all trace providers from the collection.
helpviewer_keywords: ["Clear","Clear method [PLA]","Clear method [PLA]","ITraceDataProviderCollection interface","ITraceDataProviderCollection interface [PLA]","Clear method","ITraceDataProviderCollection.Clear","ITraceDataProviderCollection::Clear","base.itracedataprovidercollection_clear","pla.itracedataprovidercollection_clear","pla/ITraceDataProviderCollection::Clear"]
old-location: pla\itracedataprovidercollection_clear.htm
tech.root: PLA
ms.assetid: aee595c2-bffc-4c79-89b3-b83f75e58d89
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [PLA], Clear method [PLA],ITraceDataProviderCollection interface, ITraceDataProviderCollection interface [PLA],Clear method, ITraceDataProviderCollection.Clear, ITraceDataProviderCollection::Clear, base.itracedataprovidercollection_clear, pla.itracedataprovidercollection_clear, pla/ITraceDataProviderCollection::Clear
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITraceDataProviderCollection::Clear
 - pla/ITraceDataProviderCollection::Clear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataProviderCollection.Clear
---

# ITraceDataProviderCollection::Clear


## -description

Removes all trace providers from the collection.



## -returns

Returns S_OK if successful.

## -remarks

Note that by removing the providers from the collection, you are also removing the providers from the trace data collector.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-remove">ITraceDataProviderCollection::Remove</a>
