---
UID: NN:pla.ITraceDataProviderCollection
title: ITraceDataProviderCollection (pla.h)
description: Manages a collection of TraceDataProvider objects.To get this interface, access the ITraceDataCollector::TraceDataProviders property.You can also call the CoCreateInstance function to create a new instance of the TraceDataProviderCollection object.
helpviewer_keywords: ["ITraceDataProviderCollection","ITraceDataProviderCollection interface [PLA]","ITraceDataProviderCollection interface [PLA]","described","base.itracedataprovidercollection","pla.itracedataprovidercollection","pla/ITraceDataProviderCollection"]
old-location: pla\itracedataprovidercollection.htm
tech.root: PLA
ms.assetid: 74300222-dca4-4871-bae3-0c3182fbc539
ms.date: 12/05/2018
ms.keywords: ITraceDataProviderCollection, ITraceDataProviderCollection interface [PLA], ITraceDataProviderCollection interface [PLA],described, base.itracedataprovidercollection, pla.itracedataprovidercollection, pla/ITraceDataProviderCollection
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
 - ITraceDataProviderCollection
 - pla/ITraceDataProviderCollection
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
 - ITraceDataProviderCollection
---

# ITraceDataProviderCollection interface


## -description

Manages a collection of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">TraceDataProvider</a> objects.

To get this interface, access the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_tracedataproviders">ITraceDataCollector::TraceDataProviders</a> property.

You can also call the <b>CoCreateInstance</b> function to create a new instance of the <b>TraceDataProviderCollection</b> object. Pass __uuidof(TraceDataProviderCollection) as the class identifier and __uuidof(<b>ITraceDataProviderCollection</b>) as the interface identifier.

To populate the collection with registered providers, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-gettracedataproviders">ITraceDataProviderCollection::GetTraceDataProviders</a> method.

## -inheritance

The <b>ITraceDataProviderCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITraceDataProviderCollection</b> also has these types of members:

## -remarks

To create the object from a script, use the Pla.TraceDataProviderCollection program identifier.
