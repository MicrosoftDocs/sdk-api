---
UID: NF:pla.ITraceDataProviderCollection.GetTraceDataProvidersByProcess
title: ITraceDataProviderCollection::GetTraceDataProvidersByProcess (pla.h)
description: Populates the collection with the list of providers that have been registered by the specified process.
helpviewer_keywords: ["GetTraceDataProvidersByProcess","GetTraceDataProvidersByProcess method [PLA]","GetTraceDataProvidersByProcess method [PLA]","ITraceDataProviderCollection interface","ITraceDataProviderCollection interface [PLA]","GetTraceDataProvidersByProcess method","ITraceDataProviderCollection.GetTraceDataProvidersByProcess","ITraceDataProviderCollection::GetTraceDataProvidersByProcess","pla.itracedataprovidercollection_gettracedataprovidersbyprocess","pla/ITraceDataProviderCollection::GetTraceDataProvidersByProcess"]
old-location: pla\itracedataprovidercollection_gettracedataprovidersbyprocess.htm
tech.root: PLA
ms.assetid: bc8b6aeb-7239-4bce-8616-62f87b84ae6c
ms.date: 12/05/2018
ms.keywords: GetTraceDataProvidersByProcess, GetTraceDataProvidersByProcess method [PLA], GetTraceDataProvidersByProcess method [PLA],ITraceDataProviderCollection interface, ITraceDataProviderCollection interface [PLA],GetTraceDataProvidersByProcess method, ITraceDataProviderCollection.GetTraceDataProvidersByProcess, ITraceDataProviderCollection::GetTraceDataProvidersByProcess, pla.itracedataprovidercollection_gettracedataprovidersbyprocess, pla/ITraceDataProviderCollection::GetTraceDataProvidersByProcess
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
 - ITraceDataProviderCollection::GetTraceDataProvidersByProcess
 - pla/ITraceDataProviderCollection::GetTraceDataProvidersByProcess
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
 - ITraceDataProviderCollection.GetTraceDataProvidersByProcess
---

# ITraceDataProviderCollection::GetTraceDataProvidersByProcess


## -description

Populates the collection with the list of providers that have been registered by the specified process.

## -parameters

### -param Server [in]

The computer whose registered trace providers you want to enumerate. You can specify a computer name, a fully qualified domain name, or an IP address (IPv4 or IPv6 format). If <b>NULL</b>, PLA enumerates the providers on the local computer.

### -param Pid [in]

The process identifier of the process that registered the providers.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-gettracedataproviders">ITraceDataProviderCollection::GetTraceDataProviders</a>