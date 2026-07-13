---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProviderQuery
title: IFunctionDiscoveryProviderQuery (functiondiscoveryprovider.h)
description: This interface is passed to all IFunctionDiscoveryProvider::Query method calls and contains query definition information. Providers should use this to determine what the constraints are for each query request they receive.
helpviewer_keywords: ["IFunctionDiscoveryProviderQuery","IFunctionDiscoveryProviderQuery interface","IFunctionDiscoveryProviderQuery interface","described","functiondiscoveryprovider/IFunctionDiscoveryProviderQuery","ncd.ifunctiondiscoveryproviderquery"]
old-location: ncd\ifunctiondiscoveryproviderquery.htm
tech.root: ncd
ms.assetid: 97468045-faa5-4690-8db5-50ee9656517b
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProviderQuery, IFunctionDiscoveryProviderQuery interface, IFunctionDiscoveryProviderQuery interface,described, functiondiscoveryprovider/IFunctionDiscoveryProviderQuery, ncd.ifunctiondiscoveryproviderquery
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
 - IFunctionDiscoveryProviderQuery
 - functiondiscoveryprovider/IFunctionDiscoveryProviderQuery
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
 - IFunctionDiscoveryProviderQuery
---

# IFunctionDiscoveryProviderQuery interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is passed to all <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query">IFunctionDiscoveryProvider::Query</a> method calls and contains query definition information.  Providers should use this to determine what the constraints are for each query request they receive.

## -inheritance

The <b>IFunctionDiscoveryProviderQuery</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscoveryProviderQuery</b> also has these types of members:

