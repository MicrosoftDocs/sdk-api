---
UID: NF:pla.ITraceDataProviderCollection.Remove
title: ITraceDataProviderCollection::Remove (pla.h)
description: Removes a trace provider from the collection.
helpviewer_keywords: ["ITraceDataProviderCollection interface [PLA]","Remove method","ITraceDataProviderCollection.Remove","ITraceDataProviderCollection::Remove","Remove","Remove method [PLA]","Remove method [PLA]","ITraceDataProviderCollection interface","base.itracedataprovidercollection_remove","pla.itracedataprovidercollection_remove","pla/ITraceDataProviderCollection::Remove"]
old-location: pla\itracedataprovidercollection_remove.htm
tech.root: PLA
ms.assetid: 553ec66e-d38a-46cc-9b01-f4d7947eda91
ms.date: 12/05/2018
ms.keywords: ITraceDataProviderCollection interface [PLA],Remove method, ITraceDataProviderCollection.Remove, ITraceDataProviderCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],ITraceDataProviderCollection interface, base.itracedataprovidercollection_remove, pla.itracedataprovidercollection_remove, pla/ITraceDataProviderCollection::Remove
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
 - ITraceDataProviderCollection::Remove
 - pla/ITraceDataProviderCollection::Remove
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
 - ITraceDataProviderCollection.Remove
---

# ITraceDataProviderCollection::Remove


## -description

Removes a trace provider from the collection.

## -parameters

### -param vProvider [in]

The zero-based index of the trace provider to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.

## -returns

Returns S_OK if successful.

## -remarks

If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a> interface to be removed.

Note that by removing the trace provider from the collection, you are also removing the provider from the trace data collector.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-add">ITraceDataProviderCollection::Add</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-clear">ITraceDataProviderCollection::Clear</a>