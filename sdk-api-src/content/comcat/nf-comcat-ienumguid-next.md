---
UID: NF:comcat.IEnumGUID.Next
title: IEnumGUID::Next (comcat.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumGUID.Next)
helpviewer_keywords: ["IEnumGUID interface [COM]","Next method","IEnumGUID.Next","IEnumGUID::Next","Next","Next method [COM]","Next method [COM]","IEnumGUID interface","_com_ienumguid_next","com.ienumguid_next","comcat/IEnumGUID::Next"]
old-location: com\ienumguid_next.htm
tech.root: com
ms.assetid: d32e02c7-1109-40cc-bf36-d224fa59fe20
ms.date: 12/05/2018
ms.keywords: IEnumGUID interface [COM],Next method, IEnumGUID.Next, IEnumGUID::Next, Next, Next method [COM], Next method [COM],IEnumGUID interface, _com_ienumguid_next, com.ienumguid_next, comcat/IEnumGUID::Next
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
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
 - IEnumGUID::Next
 - comcat/IEnumGUID::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - IEnumGUID.Next
---

# IEnumGUID::Next


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

<a href="/windows/desktop/api/comcat/nn-comcat-ienumguid">IEnumGUID</a>
