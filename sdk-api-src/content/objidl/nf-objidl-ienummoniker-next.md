---
UID: NF:objidl.IEnumMoniker.Next
title: IEnumMoniker::Next (objidl.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumMoniker.Next)
helpviewer_keywords: ["IEnumMoniker interface [COM]","Next method","IEnumMoniker.Next","IEnumMoniker::Next","Next","Next method [COM]","Next method [COM]","IEnumMoniker interface","_ole_ienummoniker_next","com.ienummoniker_next","objidl/IEnumMoniker::Next"]
old-location: com\ienummoniker_next.htm
tech.root: com
ms.assetid: ab4fd626-bddc-42b4-b279-b89d1f79b1e1
ms.date: 12/05/2018
ms.keywords: IEnumMoniker interface [COM],Next method, IEnumMoniker.Next, IEnumMoniker::Next, Next, Next method [COM], Next method [COM],IEnumMoniker interface, _ole_ienummoniker_next, com.ienummoniker_next, objidl/IEnumMoniker::Next
req.header: objidl.h
req.include-header: 
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
 - IEnumMoniker::Next
 - objidl/IEnumMoniker::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IEnumMoniker.Next
---

# IEnumMoniker::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

### -param rgelt [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>, and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> through each pointer enumerated. If <i>celt</i> is greater than 1, the caller must also pass a non-<b>NULL</b> pointer passed to <i>pceltFetched</i> to know how many pointers to release.

### -param pceltFetched [in, out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested. This parameter can be <b>NULL</b> if <i>celt</i> is 1.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
