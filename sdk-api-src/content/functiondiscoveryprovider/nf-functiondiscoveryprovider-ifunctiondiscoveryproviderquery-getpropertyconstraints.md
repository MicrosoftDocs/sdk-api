---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderQuery.GetPropertyConstraints
title: IFunctionDiscoveryProviderQuery::GetPropertyConstraints (functiondiscoveryprovider.h)
description: Retrieves the current property constraints.
helpviewer_keywords: ["GetPropertyConstraints","GetPropertyConstraints method","GetPropertyConstraints method","IFunctionDiscoveryProviderQuery interface","IFunctionDiscoveryProviderQuery interface","GetPropertyConstraints method","IFunctionDiscoveryProviderQuery.GetPropertyConstraints","IFunctionDiscoveryProviderQuery::GetPropertyConstraints","functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::GetPropertyConstraints","ncd.ifunctiondiscoveryproviderquery_getpropertyconstraints"]
old-location: ncd\ifunctiondiscoveryproviderquery_getpropertyconstraints.htm
tech.root: ncd
ms.assetid: d8a45d1b-fb1e-4288-a42a-b967cc9b4533
ms.date: 12/05/2018
ms.keywords: GetPropertyConstraints, GetPropertyConstraints method, GetPropertyConstraints method,IFunctionDiscoveryProviderQuery interface, IFunctionDiscoveryProviderQuery interface,GetPropertyConstraints method, IFunctionDiscoveryProviderQuery.GetPropertyConstraints, IFunctionDiscoveryProviderQuery::GetPropertyConstraints, functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::GetPropertyConstraints, ncd.ifunctiondiscoveryproviderquery_getpropertyconstraints
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
 - IFunctionDiscoveryProviderQuery::GetPropertyConstraints
 - functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::GetPropertyConstraints
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
 - IFunctionDiscoveryProviderQuery.GetPropertyConstraints
---

# IFunctionDiscoveryProviderQuery::GetPropertyConstraints


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the current property constraints.

## -parameters

### -param ppIProviderPropertyConstraints [out]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderpropertyconstraintcollection">IProviderPropertyConstraintCollection</a> interface pointer that receives the collection of property constraints.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Function Discovery will apply all property constraints to the results returned by the provider, but it is more efficient if the provider can apply the property constraints to the results.

  The provider should examine all constraints to determine the query to perform.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderquery">IFunctionDiscoveryProviderQuery</a>