---
UID: NF:ocidl.IEnumConnections.Next
title: IEnumConnections::Next (ocidl.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumConnections.Next)
helpviewer_keywords: ["IEnumConnections interface [COM]","Next method","IEnumConnections.Next","IEnumConnections::Next","Next","Next method [COM]","Next method [COM]","IEnumConnections interface","_com_ienumconnections_next","com.ienumconnections_next","ocidl/IEnumConnections::Next"]
old-location: com\ienumconnections_next.htm
tech.root: com
ms.assetid: af58f961-1182-43fc-95ce-4afb251b9b08
ms.date: 12/05/2018
ms.keywords: IEnumConnections interface [COM],Next method, IEnumConnections.Next, IEnumConnections::Next, Next, Next method [COM], Next method [COM],IEnumConnections interface, _com_ienumconnections_next, com.ienumconnections_next, ocidl/IEnumConnections::Next
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
 - IEnumConnections::Next
 - ocidl/IEnumConnections::Next
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
 - IEnumConnections.Next
---

## -description

Retrieves the specified number of items in the enumeration sequence. An item corresponds to a [CONNECTDATA](/windows/win32/api/ocidl/ns-ocidl-connectdata) structure.

## -parameters

### -param cConnections [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

### -param rgcd [out]

An array of enumerated items.

The enumerator is responsible for allocating any memory, and the caller is responsible for freeing it. If <i>celt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pceltFetched</i> to know how many pointers to release.

### -param pcFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -remarks

After this method returns successfully, the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> (see the <b>pUnk</b> member of <a href="/windows/desktop/api/ocidl/ns-ocidl-connectdata">CONNECTDATA</a>) for each element in the array. If <i>cConnections</i> is greater than one, the caller must also pass a non-NULL pointer to <i>lpcFetched</i> to get the number of pointers it has to be released.

E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the array are valid on exit, and therefore no release is required.

## -see-also

<a href="/windows/desktop/api/ocidl/ns-ocidl-connectdata">CONNECTDATA</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
