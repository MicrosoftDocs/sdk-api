---
UID: NN:pla.ITraceDataProvider
title: ITraceDataProvider (pla.h)
description: Specifies a trace provider to enable in the trace session.
helpviewer_keywords: ["ITraceDataProvider","ITraceDataProvider interface [PLA]","ITraceDataProvider interface [PLA]","described","base.itracedataprovider","pla.itracedataprovider","pla/ITraceDataProvider"]
old-location: pla\itracedataprovider.htm
tech.root: PLA
ms.assetid: bd2a49c1-8e18-4a14-a797-07f2b9c25812
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider, ITraceDataProvider interface [PLA], ITraceDataProvider interface [PLA],described, base.itracedataprovider, pla.itracedataprovider, pla/ITraceDataProvider
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
 - ITraceDataProvider
 - pla/ITraceDataProvider
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
 - ITraceDataProvider
---

# ITraceDataProvider interface


## -description

Specifies a trace provider to enable in the trace session.

To get this interface, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-createtracedataprovider">ITraceDataProviderCollection::CreateTraceDataProvider</a> method.

You can also use XML to define the provider. For more information, see the Remarks section of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>.

## -inheritance

The <b>ITraceDataProvider</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITraceDataProvider</b> also has these types of members:

## -remarks

If you want to retrieve only the display name or GUID of a specific provider or  retrieve only the list of processes registered as that provider, you can get this interface by calling the <b>CoCreateInstance</b> function and passing __uuidof(TraceDataProvider) as the class identifier and __uuidof(ITraceDataProvider) as the interface identifier. To create the object from a script for this purpose, use the Pla.TraceDataProvider program identifier. 

Do not use the <b>CoCreateInstance</b> function if you are going to add the interface to the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a> collection.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_tracedataproviders">ITraceDataCollector::TraceDataProviders</a>



<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>
