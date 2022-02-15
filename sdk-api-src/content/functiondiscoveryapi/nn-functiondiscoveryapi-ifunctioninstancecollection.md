---
UID: NN:functiondiscoveryapi.IFunctionInstanceCollection
title: IFunctionInstanceCollection (functiondiscoveryapi.h)
description: Represents a group of IFunctionInstance objects returned as the result of a query or get instance request.
helpviewer_keywords: ["IFunctionInstanceCollection","IFunctionInstanceCollection interface","IFunctionInstanceCollection interface","described","functiondiscoveryapi/IFunctionInstanceCollection","ncd.ifunctioninstancecollection"]
old-location: ncd\ifunctioninstancecollection.htm
tech.root: ncd
ms.assetid: 8ac1a406-92f3-4e39-985e-ab8fa7d28751
ms.date: 12/05/2018
ms.keywords: IFunctionInstanceCollection, IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,described, functiondiscoveryapi/IFunctionInstanceCollection, ncd.ifunctioninstancecollection
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionInstanceCollection
 - functiondiscoveryapi/IFunctionInstanceCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstanceCollection
---

# IFunctionInstanceCollection interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface represents a group of <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> objects returned as the result of a query or get instance request through one of the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a> methods; client program do not create these collections themselves.

## -inheritance

The <b>IFunctionInstanceCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionInstanceCollection</b> also has these types of members:

## -remarks

The <b>IFunctionInstanceCollection</b> interface allows a client program to enumerate a collection of  <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> objects.
