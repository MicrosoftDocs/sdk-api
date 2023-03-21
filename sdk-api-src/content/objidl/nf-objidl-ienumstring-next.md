---
UID: NF:objidl.IEnumString.Next
title: IEnumString::Next (objidl.h)
description: The IEnumString::Next method (objidl.h) retrieves the specified number of items in the enumeration sequence.
helpviewer_keywords: ["IEnumString interface [COM]","Next method","IEnumString.Next","IEnumString::Next","Next","Next method [COM]","Next method [COM]","IEnumString interface","_com_ienumstring_next","com.ienumstring_next","objidlbase/IEnumString::Next"]
old-location: com\ienumstring_next.htm
tech.root: com
ms.assetid: e08edeac-92c3-4947-9f55-224aab237453
ms.date: 08/12/2022
ms.keywords: IEnumString interface [COM],Next method, IEnumString.Next, IEnumString::Next, Next, Next method [COM], Next method [COM],IEnumString interface, _com_ienumstring_next, com.ienumstring_next, objidlbase/IEnumString::Next
req.header: objidl.h
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
 - IEnumString::Next
 - objidl/IEnumString::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IEnumString.Next
---

# IEnumString::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

### -param rgelt [out]

An array of enumerated items.

The enumerator is responsible for allocating any memory, and the caller is responsible for freeing it. If <i>celt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pceltFetched</i> to know how many pointers to release.

### -param pceltFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>
