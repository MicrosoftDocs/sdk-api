---
UID: NN:functiondiscoveryapi.IFunctionInstanceQuery
title: IFunctionInstanceQuery (functiondiscoveryapi.h)
description: Implements the asynchronous query for a function instance based on category and subcategory.
helpviewer_keywords: ["IFunctionInstanceQuery","IFunctionInstanceQuery interface","IFunctionInstanceQuery interface","described","functiondiscoveryapi/IFunctionInstanceQuery","ncd.ifunctioninstancequery"]
old-location: ncd\ifunctioninstancequery.htm
tech.root: ncd
ms.assetid: 03343d85-c0db-436d-bedc-c001b1886173
ms.date: 12/05/2018
ms.keywords: IFunctionInstanceQuery, IFunctionInstanceQuery interface, IFunctionInstanceQuery interface,described, functiondiscoveryapi/IFunctionInstanceQuery, ncd.ifunctioninstancequery
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
 - IFunctionInstanceQuery
 - functiondiscoveryapi/IFunctionInstanceQuery
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
 - IFunctionInstanceQuery
---

# IFunctionInstanceQuery interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface implements the asynchronous query for a function instance based on category and subcategory. A pointer to this interface is returned when the query is created by the client program.

## -inheritance

The <b>IFunctionInstanceQuery</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionInstanceQuery</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancequery-execute">Execute</a> method must be invoked by the client program before any data can be retrieved from the query object.

## -see-also

<a href="/previous-versions/windows/desktop/fundisc/function-discovery-queries">Function Discovery Queries</a>
