---
UID: NF:pla.ITraceDataProviderCollection.GetTraceDataProviders
title: ITraceDataProviderCollection::GetTraceDataProviders (pla.h)
description: Populates the collection with registered trace providers.
helpviewer_keywords: ["GetTraceDataProviders","GetTraceDataProviders method [PLA]","GetTraceDataProviders method [PLA]","ITraceDataProviderCollection interface","ITraceDataProviderCollection interface [PLA]","GetTraceDataProviders method","ITraceDataProviderCollection.GetTraceDataProviders","ITraceDataProviderCollection::GetTraceDataProviders","base.itracedataprovidercollection_gettracedataproviders","pla.itracedataprovidercollection_gettracedataproviders","pla/ITraceDataProviderCollection::GetTraceDataProviders"]
old-location: pla\itracedataprovidercollection_gettracedataproviders.htm
tech.root: PLA
ms.assetid: ff35087e-be55-42e8-96e9-c923d06248d8
ms.date: 12/05/2018
ms.keywords: GetTraceDataProviders, GetTraceDataProviders method [PLA], GetTraceDataProviders method [PLA],ITraceDataProviderCollection interface, ITraceDataProviderCollection interface [PLA],GetTraceDataProviders method, ITraceDataProviderCollection.GetTraceDataProviders, ITraceDataProviderCollection::GetTraceDataProviders, base.itracedataprovidercollection_gettracedataproviders, pla.itracedataprovidercollection_gettracedataproviders, pla/ITraceDataProviderCollection::GetTraceDataProviders
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
 - ITraceDataProviderCollection::GetTraceDataProviders
 - pla/ITraceDataProviderCollection::GetTraceDataProviders
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
 - ITraceDataProviderCollection.GetTraceDataProviders
---

# ITraceDataProviderCollection::GetTraceDataProviders


## -description

Populates the collection with registered trace providers.

## -parameters

### -param server [in]

The computer whose registered trace providers you want to enumerate. You can specify a computer name, a fully qualified domain name, or an IP address (IPv4 or IPv6 format). If <b>NULL</b>, PLA enumerates the providers on the local computer.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-gettracedataprovidersbyprocess">ITraceDataProviderCollection::GetTraceDataProvidersByProcess</a>