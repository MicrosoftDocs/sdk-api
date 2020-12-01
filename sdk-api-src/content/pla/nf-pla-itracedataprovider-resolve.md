---
UID: NF:pla.ITraceDataProvider.Resolve
title: ITraceDataProvider::Resolve (pla.h)
description: Merges the details about a provider with this instance.
helpviewer_keywords: ["ITraceDataProvider interface [PLA]","Resolve method","ITraceDataProvider.Resolve","ITraceDataProvider::Resolve","Resolve","Resolve method [PLA]","Resolve method [PLA]","ITraceDataProvider interface","base.itracedataprovider_resolve","pla.itracedataprovider_resolve","pla/ITraceDataProvider::Resolve"]
old-location: pla\itracedataprovider_resolve.htm
tech.root: PLA
ms.assetid: cabe7207-30f9-4382-bc29-b435d6e4c218
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider interface [PLA],Resolve method, ITraceDataProvider.Resolve, ITraceDataProvider::Resolve, Resolve, Resolve method [PLA], Resolve method [PLA],ITraceDataProvider interface, base.itracedataprovider_resolve, pla.itracedataprovider_resolve, pla/ITraceDataProvider::Resolve
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
 - ITraceDataProvider::Resolve
 - pla/ITraceDataProvider::Resolve
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
 - ITraceDataProvider.Resolve
---

# ITraceDataProvider::Resolve


## -description

Merges the details about a provider with this instance.

## -parameters

### -param pFrom [in]

The interface of the provider to merge with this instance.

## -returns

Returns S_OK if successful.

## -remarks

You can specify an interface of a provider or a collection that contains the provider. If you specify a collection, the method finds the matching provider.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>