---
UID: NF:ocidl.IEnumConnectionPoints.Clone
title: IEnumConnectionPoints::Clone (ocidl.h)
description: Creates a new enumerator that contains the same enumeration state as the current one. (IEnumConnectionPoints.Clone)
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumConnectionPoints interface","IEnumConnectionPoints interface [COM]","Clone method","IEnumConnectionPoints.Clone","IEnumConnectionPoints::Clone","_com_ienumconnectionpoints_clone","com.ienumconnectionpoints_clone","ocidl/IEnumConnectionPoints::Clone"]
old-location: com\ienumconnectionpoints_clone.htm
tech.root: com
ms.assetid: 47dfd670-57f7-4fb1-bd61-65dd4a3bc6c2
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumConnectionPoints interface, IEnumConnectionPoints interface [COM],Clone method, IEnumConnectionPoints.Clone, IEnumConnectionPoints::Clone, _com_ienumconnectionpoints_clone, com.ienumconnectionpoints_clone, ocidl/IEnumConnectionPoints::Clone
req.header: ocidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IEnumConnectionPoints::Clone
 - ocidl/IEnumConnectionPoints::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ocidl.h
api_name:
 - IEnumConnectionPoints.Clone
---

# IEnumConnectionPoints::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppEnum [out]

A pointer to the cloned enumerator object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>
