---
UID: NF:objidl.IEnumSTATDATA.Next
title: IEnumSTATDATA::Next (objidl.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumSTATDATA.Next)
helpviewer_keywords: ["IEnumSTATDATA interface [COM]","Next method","IEnumSTATDATA.Next","IEnumSTATDATA::Next","Next","Next method [COM]","Next method [COM]","IEnumSTATDATA interface","_ole_ienumstatdata_next","com.ienumstatdata_next","objidl/IEnumSTATDATA::Next"]
old-location: com\ienumstatdata_next.htm
tech.root: com
ms.assetid: 8258b6f4-15d7-4da2-96d1-d1ce36a31c1c
ms.date: 12/05/2018
ms.keywords: IEnumSTATDATA interface [COM],Next method, IEnumSTATDATA.Next, IEnumSTATDATA::Next, Next, Next method [COM], Next method [COM],IEnumSTATDATA interface, _ole_ienumstatdata_next, com.ienumstatdata_next, objidl/IEnumSTATDATA::Next
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
 - IEnumSTATDATA::Next
 - objidl/IEnumSTATDATA::Next
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
 - IEnumSTATDATA.Next
---

# IEnumSTATDATA::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

### -param rgelt [out]

An array of enumerated items.

The enumerator is responsible for allocating any memory, and the caller is responsible for freeing it. If <i>celt</i> is greater than 1, the caller must also pass a non-<b>NULL</b> pointer passed to <i>pceltFetched</i> to know how many pointers to release.

### -param pceltFetched [in, out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested. This parameter can be <b>NULL</b> if <i>celt</i> is 1.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a>
