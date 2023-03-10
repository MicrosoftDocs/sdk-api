---
UID: NF:oleidl.IEnumOLEVERB.Next
title: IEnumOLEVERB::Next (oleidl.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumOLEVERB.Next)
helpviewer_keywords: ["IEnumOLEVERB interface [COM]","Next method","IEnumOLEVERB.Next","IEnumOLEVERB::Next","Next","Next method [COM]","Next method [COM]","IEnumOLEVERB interface","_ole_ienumoleverb_next","com.ienumoleverb_next","oleidl/IEnumOLEVERB::Next"]
old-location: com\ienumoleverb_next.htm
tech.root: com
ms.assetid: bb934017-9054-42b5-89d4-a24f12829503
ms.date: 12/05/2018
ms.keywords: IEnumOLEVERB interface [COM],Next method, IEnumOLEVERB.Next, IEnumOLEVERB::Next, Next, Next method [COM], Next method [COM],IEnumOLEVERB interface, _ole_ienumoleverb_next, com.ienumoleverb_next, oleidl/IEnumOLEVERB::Next
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IEnumOLEVERB::Next
 - oleidl/IEnumOLEVERB::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IEnumOLEVERB.Next
---

# IEnumOLEVERB::Next


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

<a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>



<a href="/windows/desktop/api/oleidl/ns-oleidl-oleverb">OLEVERB</a>
