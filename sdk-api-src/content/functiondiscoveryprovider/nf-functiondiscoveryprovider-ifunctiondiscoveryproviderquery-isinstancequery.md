---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderQuery.IsInstanceQuery
title: IFunctionDiscoveryProviderQuery::IsInstanceQuery (functiondiscoveryprovider.h)
description: Determines whether a query is for a single function instance or multiple function instances.
helpviewer_keywords: ["IFunctionDiscoveryProviderQuery interface","IsInstanceQuery method","IFunctionDiscoveryProviderQuery.IsInstanceQuery","IFunctionDiscoveryProviderQuery::IsInstanceQuery","IsInstanceQuery","IsInstanceQuery method","IsInstanceQuery method","IFunctionDiscoveryProviderQuery interface","functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::IsInstanceQuery","ncd.ifunctiondiscoveryproviderquery_isinstancequery"]
old-location: ncd\ifunctiondiscoveryproviderquery_isinstancequery.htm
tech.root: ncd
ms.assetid: 5cd4288f-8cb8-451b-b982-4b9dcf31f66a
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProviderQuery interface,IsInstanceQuery method, IFunctionDiscoveryProviderQuery.IsInstanceQuery, IFunctionDiscoveryProviderQuery::IsInstanceQuery, IsInstanceQuery, IsInstanceQuery method, IsInstanceQuery method,IFunctionDiscoveryProviderQuery interface, functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::IsInstanceQuery, ncd.ifunctiondiscoveryproviderquery_isinstancequery
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionDiscoveryProviderQuery::IsInstanceQuery
 - functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::IsInstanceQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProviderQuery.IsInstanceQuery
---

# IFunctionDiscoveryProviderQuery::IsInstanceQuery


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a query is for a single function instance or multiple function instances.

## -parameters

### -param pisInstanceQuery [out]

If this parameter is <b>TRUE</b>, there is a provider instance identifier constraint in the query constraints collection.

### -param ppszConstraintValue [out]

The value of the provider instance identifier constraint.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderquery">IFunctionDiscoveryProviderQuery</a>