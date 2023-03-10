---
UID: NF:ocidl.IEnumConnectionPoints.Next
title: IEnumConnectionPoints::Next (ocidl.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumConnectionPoints.Next)
helpviewer_keywords: ["IEnumConnectionPoints interface [COM]","Next method","IEnumConnectionPoints.Next","IEnumConnectionPoints::Next","Next","Next method [COM]","Next method [COM]","IEnumConnectionPoints interface","_com_ienumconnectionpoints_next","com.ienumconnectionpoints_next","ocidl/IEnumConnectionPoints::Next"]
old-location: com\ienumconnectionpoints_next.htm
tech.root: com
ms.assetid: 954bd587-75ce-4216-85c9-f1382414a979
ms.date: 12/05/2018
ms.keywords: IEnumConnectionPoints interface [COM],Next method, IEnumConnectionPoints.Next, IEnumConnectionPoints::Next, Next, Next method [COM], Next method [COM],IEnumConnectionPoints interface, _com_ienumconnectionpoints_next, com.ienumconnectionpoints_next, ocidl/IEnumConnectionPoints::Next
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
 - IEnumConnectionPoints::Next
 - ocidl/IEnumConnectionPoints::Next
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
 - IEnumConnectionPoints.Next
---

# IEnumConnectionPoints::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param cConnections [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

### -param ppCP [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>, and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> through each pointer enumerated. If <i>cConnections</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>lpcFetched</i> to know how many pointers to release.

### -param pcFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>
