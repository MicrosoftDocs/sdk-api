---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProviderFactory
title: IFunctionDiscoveryProviderFactory (functiondiscoveryprovider.h)
description: Provides factory methods to create Function Discovery objects.
helpviewer_keywords: ["IFunctionDiscoveryProviderFactory","IFunctionDiscoveryProviderFactory interface","IFunctionDiscoveryProviderFactory interface","described","functiondiscoveryprovider/IFunctionDiscoveryProviderFactory","ncd.ifunctiondiscoveryproviderfactory"]
old-location: ncd\ifunctiondiscoveryproviderfactory.htm
tech.root: ncd
ms.assetid: 576db617-0bca-4b46-839b-0f133f28cacb
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProviderFactory, IFunctionDiscoveryProviderFactory interface, IFunctionDiscoveryProviderFactory interface,described, functiondiscoveryprovider/IFunctionDiscoveryProviderFactory, ncd.ifunctiondiscoveryproviderfactory
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
 - IFunctionDiscoveryProviderFactory
 - functiondiscoveryprovider/IFunctionDiscoveryProviderFactory
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
 - IFunctionDiscoveryProviderFactory
---

# IFunctionDiscoveryProviderFactory interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Provides factory methods to create Function Discovery objects.

Synchronous query results are passed using the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a> parameter of <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query">IFunctionDiscoveryProvider::Query</a> method.

## -inheritance

The <b>IFunctionDiscoveryProviderFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscoveryProviderFactory</b> also has these types of members:

