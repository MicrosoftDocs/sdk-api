---
UID: NF:pla.ITraceDataProviderCollection.Add
title: ITraceDataProviderCollection::Add (pla.h)
description: Adds a trace provider to the collection.
helpviewer_keywords: ["Add","Add method [PLA]","Add method [PLA]","ITraceDataProviderCollection interface","ITraceDataProviderCollection interface [PLA]","Add method","ITraceDataProviderCollection.Add","ITraceDataProviderCollection::Add","base.itracedataprovidercollection_add","pla.itracedataprovidercollection_add","pla/ITraceDataProviderCollection::Add"]
old-location: pla\itracedataprovidercollection_add.htm
tech.root: PLA
ms.assetid: 3214f25d-1991-439a-b237-61249a531a2b
ms.date: 12/05/2018
ms.keywords: Add, Add method [PLA], Add method [PLA],ITraceDataProviderCollection interface, ITraceDataProviderCollection interface [PLA],Add method, ITraceDataProviderCollection.Add, ITraceDataProviderCollection::Add, base.itracedataprovidercollection_add, pla.itracedataprovidercollection_add, pla/ITraceDataProviderCollection::Add
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
 - ITraceDataProviderCollection::Add
 - pla/ITraceDataProviderCollection::Add
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
 - ITraceDataProviderCollection.Add
---

# ITraceDataProviderCollection::Add


## -description

Adds a trace provider to the collection.

## -parameters

### -param pProvider [in]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a> interface of the trace provider to add to this collection.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-addrange">ITraceDataProviderCollection::AddRange</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-remove">ITraceDataProviderCollection::Remove</a>