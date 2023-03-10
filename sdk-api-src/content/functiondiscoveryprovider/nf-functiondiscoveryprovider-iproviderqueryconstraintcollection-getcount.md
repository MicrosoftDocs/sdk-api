---
UID: NF:functiondiscoveryprovider.IProviderQueryConstraintCollection.GetCount
title: IProviderQueryConstraintCollection::GetCount (functiondiscoveryprovider.h)
description: Gets the number of items in the collection. (IProviderQueryConstraintCollection.GetCount)
helpviewer_keywords: ["GetCount","GetCount method","GetCount method","IProviderQueryConstraintCollection interface","IProviderQueryConstraintCollection interface","GetCount method","IProviderQueryConstraintCollection.GetCount","IProviderQueryConstraintCollection::GetCount","functiondiscoveryprovider/IProviderQueryConstraintCollection::GetCount","ncd.iproviderqueryconstraintcollection_getcount"]
old-location: ncd\iproviderqueryconstraintcollection_getcount.htm
tech.root: ncd
ms.assetid: 401e1723-751a-490b-bcb6-d1e0f2f73dfb
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method, GetCount method,IProviderQueryConstraintCollection interface, IProviderQueryConstraintCollection interface,GetCount method, IProviderQueryConstraintCollection.GetCount, IProviderQueryConstraintCollection::GetCount, functiondiscoveryprovider/IProviderQueryConstraintCollection::GetCount, ncd.iproviderqueryconstraintcollection_getcount
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
 - IProviderQueryConstraintCollection::GetCount
 - functiondiscoveryprovider/IProviderQueryConstraintCollection::GetCount
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
 - IProviderQueryConstraintCollection.GetCount
---

# IProviderQueryConstraintCollection::GetCount


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the number of items in the collection.

## -parameters

### -param pdwCount [out]

The number of items.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-iproviderqueryconstraintcollection">IProviderQueryConstraintCollection</a>
