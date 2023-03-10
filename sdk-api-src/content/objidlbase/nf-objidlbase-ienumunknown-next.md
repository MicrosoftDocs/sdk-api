---
UID: NF:objidlbase.IEnumUnknown.Next
title: IEnumUnknown::Next (objidlbase.h)
description: The IEnumUnknown::Next (objidlbase.h) method retrieves the specified number of items in the enumeration sequence.
helpviewer_keywords: ["IEnumUnknown interface [COM]","Next method","IEnumUnknown.Next","IEnumUnknown::Next","Next","Next method [COM]","Next method [COM]","IEnumUnknown interface","_com_ienumunknown_next","com.ienumunknown_next","objidlbase/IEnumUnknown::Next"]
old-location: com\ienumunknown_next.htm
tech.root: com
ms.assetid: cef932cf-dacd-430d-8834-c41cc2d885a6
ms.date: 08/13/2022
ms.keywords: IEnumUnknown interface [COM],Next method, IEnumUnknown.Next, IEnumUnknown::Next, Next, Next method [COM], Next method [COM],IEnumUnknown interface, _com_ienumunknown_next, com.ienumunknown_next, objidlbase/IEnumUnknown::Next
req.header: objidlbase.h
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
 - IEnumUnknown::Next
 - objidlbase/IEnumUnknown::Next
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
 - IEnumUnknown.Next
---

# IEnumUnknown::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

### -param rgelt [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>, and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> through each pointer enumerated. If <i>celt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pceltFetched</i> to know how many pointers to release.

### -param pceltFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
