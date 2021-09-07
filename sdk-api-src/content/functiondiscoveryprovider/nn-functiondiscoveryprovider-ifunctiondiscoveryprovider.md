---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryProvider
title: IFunctionDiscoveryProvider (functiondiscoveryprovider.h)
description: This is the main interface implemented by a discovery provider. It is the primary interface the Function Discovery infrastructure uses to communicate with the provider and its resources.
helpviewer_keywords: ["IFunctionDiscoveryProvider","IFunctionDiscoveryProvider interface","IFunctionDiscoveryProvider interface","described","functiondiscoveryprovider/IFunctionDiscoveryProvider","ncd.ifunctiondiscoveryprovider"]
old-location: ncd\ifunctiondiscoveryprovider.htm
tech.root: ncd
ms.assetid: e0019d0d-1495-4a0e-a7d9-7772046a4a26
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider, IFunctionDiscoveryProvider interface, IFunctionDiscoveryProvider interface,described, functiondiscoveryprovider/IFunctionDiscoveryProvider, ncd.ifunctiondiscoveryprovider
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
 - IFunctionDiscoveryProvider
 - functiondiscoveryprovider/IFunctionDiscoveryProvider
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
 - IFunctionDiscoveryProvider
---

# IFunctionDiscoveryProvider interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This is the main interface implemented by a discovery provider. It is the primary interface the Function Discovery infrastructure uses to communicate with the provider and its resources.

You should only implement and use this interface if you are writing a discovery provider. You should only write a discovery provider if you must discover devices using a method that is not supported by the <a href="/previous-versions/windows/desktop/fundisc/built-in-providers">built-in providers</a>.  

If you are writing a client program that discovers and queries devices, use the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a> interface instead.

The <a href="/previous-versions/windows/desktop/fundisc/function-discovery-provider-sample">Function Discovery Provider Sample</a> implements the <b>IFunctionDiscoveryProvider</b> interface.

## -inheritance

The <b>IFunctionDiscoveryProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionDiscoveryProvider</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/fundisc/function-discovery-provider-sample">Function Discovery Provider Sample</a>



<a href="/previous-versions/windows/desktop/fundisc/using-function-discovery-providers">Using Function Discovery Providers</a>
