---
UID: NF:pla.ITraceDataProviderCollection.GetTraceDataProviders
title: ITraceDataProviderCollection::GetTraceDataProviders
author: windows-sdk-content
description: Populates the collection with registered trace providers.
old-location: pla\itracedataprovidercollection_gettracedataproviders.htm
tech.root: pla
ms.assetid: ff35087e-be55-42e8-96e9-c923d06248d8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTraceDataProviders, GetTraceDataProviders method [PLA], GetTraceDataProviders method [PLA],ITraceDataProviderCollection interface, ITraceDataProviderCollection interface [PLA],GetTraceDataProviders method, ITraceDataProviderCollection.GetTraceDataProviders, ITraceDataProviderCollection::GetTraceDataProviders, base.itracedataprovidercollection_gettracedataproviders, pla.itracedataprovidercollection_gettracedataproviders, pla/ITraceDataProviderCollection::GetTraceDataProviders
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataProviderCollection.GetTraceDataProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/74300222-dca4-4871-bae3-0c3182fbc539">ITraceDataProviderCollection</a>



<a href="https://msdn.microsoft.com/bc8b6aeb-7239-4bce-8616-62f87b84ae6c">ITraceDataProviderCollection::GetTraceDataProvidersByProcess</a>
 

 

