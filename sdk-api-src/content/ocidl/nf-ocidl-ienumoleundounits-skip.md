---
UID: NF:ocidl.IEnumOleUndoUnits.Skip
title: IEnumOleUndoUnits::Skip (ocidl.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumOleUndoUnits.Skip)
helpviewer_keywords: ["IEnumOleUndoUnits interface [COM]","Skip method","IEnumOleUndoUnits.Skip","IEnumOleUndoUnits::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumOleUndoUnits interface","_ole_ienumoleundounits_skip","com.ienumoleundounits_skip","ocidl/IEnumOleUndoUnits::Skip"]
old-location: com\ienumoleundounits_skip.htm
tech.root: com
ms.assetid: 53c5356d-525a-485f-9618-37efe21be687
ms.date: 12/05/2018
ms.keywords: IEnumOleUndoUnits interface [COM],Skip method, IEnumOleUndoUnits.Skip, IEnumOleUndoUnits::Skip, Skip, Skip method [COM], Skip method [COM],IEnumOleUndoUnits interface, _ole_ienumoleundounits_skip, com.ienumoleundounits_skip, ocidl/IEnumOleUndoUnits::Skip
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
 - IEnumOleUndoUnits::Skip
 - ocidl/IEnumOleUndoUnits::Skip
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
 - IEnumOleUndoUnits.Skip
---

# IEnumOleUndoUnits::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param cElt [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumoleundounits">IEnumOleUndoUnits</a>
