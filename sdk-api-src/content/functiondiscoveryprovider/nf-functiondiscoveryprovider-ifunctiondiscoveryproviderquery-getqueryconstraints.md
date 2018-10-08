---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderQuery.GetQueryConstraints
title: IFunctionDiscoveryProviderQuery::GetQueryConstraints
author: windows-sdk-content
description: Retrieves the current query constraints.
old-location: ncd\ifunctiondiscoveryproviderquery_getqueryconstraints.htm
tech.root: fundisc
ms.assetid: a8329732-79dd-4606-96c3-40534cde5fc4
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetQueryConstraints, GetQueryConstraints method, GetQueryConstraints method,IFunctionDiscoveryProviderQuery interface, IFunctionDiscoveryProviderQuery interface,GetQueryConstraints method, IFunctionDiscoveryProviderQuery.GetQueryConstraints, IFunctionDiscoveryProviderQuery::GetQueryConstraints, functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::GetQueryConstraints, ncd.ifunctiondiscoveryproviderquery_getqueryconstraints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProviderQuery.GetQueryConstraints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProviderQuery::GetQueryConstraints


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the current query constraints.


## -parameters




### -param ppIProviderQueryConstraints [out]

A pointer to an <a href="https://msdn.microsoft.com/4d8ff5b9-ec4a-4ec6-b133-3d315f9c017b">IProviderQueryConstraintCollection</a> interface pointer that receives the collection of query constraints.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Providers are expected to apply all query constraints when returning results. Providers should ignore any query constraints they do not recognize.

The provider should examine all constraints to determine the query to perform. 




## -see-also




<a href="https://msdn.microsoft.com/97468045-faa5-4690-8db5-50ee9656517b">IFunctionDiscoveryProviderQuery</a>
 

 

