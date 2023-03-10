---
UID: NF:ocidl.IEnumOleUndoUnits.Next
title: IEnumOleUndoUnits::Next (ocidl.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumOleUndoUnits.Next)
helpviewer_keywords: ["IEnumOleUndoUnits interface [COM]","Next method","IEnumOleUndoUnits.Next","IEnumOleUndoUnits::Next","Next","Next method [COM]","Next method [COM]","IEnumOleUndoUnits interface","_ole_ienumoleundounits_next","com.ienumoleundounits_next","ocidl/IEnumOleUndoUnits::Next"]
old-location: com\ienumoleundounits_next.htm
tech.root: com
ms.assetid: bd5ce157-37d1-4e27-a0d4-ed9cffeac2b3
ms.date: 12/05/2018
ms.keywords: IEnumOleUndoUnits interface [COM],Next method, IEnumOleUndoUnits.Next, IEnumOleUndoUnits::Next, Next, Next method [COM], Next method [COM],IEnumOleUndoUnits interface, _ole_ienumoleundounits_next, com.ienumoleundounits_next, ocidl/IEnumOleUndoUnits::Next
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IEnumOleUndoUnits::Next
 - ocidl/IEnumOleUndoUnits::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IEnumOleUndoUnits.Next
---

# IEnumOleUndoUnits::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param cElt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

### -param rgElt [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>, and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> through each pointer enumerated. If <i>cElt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pcEltFetched</i> to know how many pointers to release.

### -param pcEltFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.

## -returns

If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -remarks

The caller is responsible for calling the Release method for each element in the array once this method returns successfully. If cUndoUnits is greater than one, the caller must also pass a non-NULL pointer to pcFetched to get the number of pointers it has to release. 



E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the rgpcd array are valid on exit and require no release.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumoleundounits">IEnumOleUndoUnits</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a>
