---
UID: NF:comsvcs.ISecurityCallersColl.get_Item
title: ISecurityCallersColl::get_Item (comsvcs.h)
description: Retrieves a specified caller in the security callers collection.
helpviewer_keywords: ["ISecurityCallersColl interface [COM+]","get_Item method","ISecurityCallersColl.get_Item","ISecurityCallersColl::get_Item","_cos_ISecurityCallersColl_get_Item","comsvcs/ISecurityCallersColl::get_Item","cos.isecuritycallerscoll_get_item","get_Item","get_Item method [COM+]","get_Item method [COM+]","ISecurityCallersColl interface"]
old-location: cos\isecuritycallerscoll_get_item.htm
tech.root: cos
ms.assetid: 24473ebe-8d29-46cd-817d-48f24b03c405
ms.date: 12/05/2018
ms.keywords: ISecurityCallersColl interface [COM+],get_Item method, ISecurityCallersColl.get_Item, ISecurityCallersColl::get_Item, _cos_ISecurityCallersColl_get_Item, comsvcs/ISecurityCallersColl::get_Item, cos.isecuritycallerscoll_get_item, get_Item, get_Item method [COM+], get_Item method [COM+],ISecurityCallersColl interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ISecurityCallersColl::get_Item
 - comsvcs/ISecurityCallersColl::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityCallersColl.get_Item
---

# ISecurityCallersColl::get_Item


## -description

Retrieves a specified caller in the security callers collection.

## -parameters

### -param lIndex [in]

The name of the caller to retrieve. See Remarks for information about the available callers.

### -param pObj [out]

A reference to the retrieved caller.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The security callers collection represents a chain of callers that cross security boundaries. These callers are also known as upstream callers.

Each item in this collection is a <a href="/windows/desktop/cossdk/securityidentity">SecurityIdentity</a> object. To obtain an item in this collection, use the Item property of the <a href="/windows/desktop/cossdk/securitycallers">SecurityCallers</a> collection object, specifying an integer index value between 0 and the number of callers, minus 1, in the collection. To retrieve the direct caller, this index value should be 0, and to retrieve the original caller, the index can be either -1 or the number of callers minus 1.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallerscoll">ISecurityCallersColl</a>