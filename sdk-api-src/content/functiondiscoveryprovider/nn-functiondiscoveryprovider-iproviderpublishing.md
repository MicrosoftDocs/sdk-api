---
UID: NN:functiondiscoveryprovider.IProviderPublishing
title: IProviderPublishing (functiondiscoveryprovider.h)
description: Is implemented by a discovery provider to enable a client program to add and remove function instances.
helpviewer_keywords: ["IProviderPublishing","IProviderPublishing interface","IProviderPublishing interface","described","functiondiscoveryprovider/IProviderPublishing","ncd.iproviderpublishing"]
old-location: ncd\iproviderpublishing.htm
tech.root: ncd
ms.assetid: 7647db1b-88c8-44f3-b2af-a61dad4790f6
ms.date: 12/05/2018
ms.keywords: IProviderPublishing, IProviderPublishing interface, IProviderPublishing interface,described, functiondiscoveryprovider/IProviderPublishing, ncd.iproviderpublishing
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
 - IProviderPublishing
 - functiondiscoveryprovider/IProviderPublishing
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
 - IProviderPublishing
---

# IProviderPublishing interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is implemented by a discovery provider to enable a client program to add and remove function instances.

## -inheritance

The <b>IProviderPublishing</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProviderPublishing</b> also has these types of members:

## -remarks

Clients access the function instance through <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-addinstance">IFunctionDiscovery::AddInstance</a> and <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-removeinstance">IFunctionDiscovery::RemoveInstance</a>.

The <b>IProviderPublishing</b> interface can only be implemented by discovery providers that support category change notification. At this time only PnP providers support change notification.
