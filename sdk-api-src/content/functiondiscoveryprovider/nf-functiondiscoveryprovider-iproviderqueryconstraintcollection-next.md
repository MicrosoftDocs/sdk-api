---
UID: NF:functiondiscoveryprovider.IProviderQueryConstraintCollection.Next
title: IProviderQueryConstraintCollection::Next (functiondiscoveryprovider.h)
description: Gets the name and value of the next query constraint in the collection.
helpviewer_keywords: ["IProviderQueryConstraintCollection interface","Next method","IProviderQueryConstraintCollection.Next","IProviderQueryConstraintCollection::Next","Next","Next method","Next method","IProviderQueryConstraintCollection interface","functiondiscoveryprovider/IProviderQueryConstraintCollection::Next","ncd.iproviderqueryconstraintcollection_next"]
old-location: ncd\iproviderqueryconstraintcollection_next.htm
tech.root: ncd
ms.assetid: 5dd03e98-5367-4434-aa68-be36cb7aaf24
ms.date: 12/05/2018
ms.keywords: IProviderQueryConstraintCollection interface,Next method, IProviderQueryConstraintCollection.Next, IProviderQueryConstraintCollection::Next, Next, Next method, Next method,IProviderQueryConstraintCollection interface, functiondiscoveryprovider/IProviderQueryConstraintCollection::Next, ncd.iproviderqueryconstraintcollection_next
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
 - IProviderQueryConstraintCollection::Next
 - functiondiscoveryprovider/IProviderQueryConstraintCollection::Next
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
 - IProviderQueryConstraintCollection.Next
---

# IProviderQueryConstraintCollection::Next


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the name and value of the next query  constraint in the collection.

## -parameters

### -param ppszConstraintName [out]

The constraint name.

### -param ppszConstraintValue [out]

The constraint value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderqueryconstraintcollection">IProviderQueryConstraintCollection</a>