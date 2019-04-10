---
UID: NF:pla.ITraceDataProviderCollection.Remove
title: ITraceDataProviderCollection::Remove (pla.h)
author: windows-sdk-content
description: Removes a trace provider from the collection.
old-location: pla\itracedataprovidercollection_remove.htm
tech.root: PLA
ms.assetid: 553ec66e-d38a-46cc-9b01-f4d7947eda91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITraceDataProviderCollection interface [PLA],Remove method, ITraceDataProviderCollection.Remove, ITraceDataProviderCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],ITraceDataProviderCollection interface, base.itracedataprovidercollection_remove, pla.itracedataprovidercollection_remove, pla/ITraceDataProviderCollection::Remove
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
 - ITraceDataProviderCollection.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a> interface to be removed.

Note that by removing the trace provider from the collection, you are also removing the provider from the trace data collector.




## -see-also




<a href="https://msdn.microsoft.com/74300222-dca4-4871-bae3-0c3182fbc539">ITraceDataProviderCollection</a>



<a href="https://msdn.microsoft.com/3214f25d-1991-439a-b237-61249a531a2b">ITraceDataProviderCollection::Add</a>



<a href="https://msdn.microsoft.com/aee595c2-bffc-4c79-89b3-b83f75e58d89">ITraceDataProviderCollection::Clear</a>
 

 

