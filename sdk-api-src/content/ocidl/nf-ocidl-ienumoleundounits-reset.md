---
UID: NF:ocidl.IEnumOleUndoUnits.Reset
title: IEnumOleUndoUnits::Reset (ocidl.h)
description: Resets the enumeration sequence to the beginning. (IEnumOleUndoUnits.Reset)
helpviewer_keywords: ["IEnumOleUndoUnits interface [COM]","Reset method","IEnumOleUndoUnits.Reset","IEnumOleUndoUnits::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumOleUndoUnits interface","_ole_ienumoleundounits_reset","com.ienumoleundounits_reset","ocidl/IEnumOleUndoUnits::Reset"]
old-location: com\ienumoleundounits_reset.htm
tech.root: com
ms.assetid: 14336909-539c-41ac-a3a6-73be04fa72d1
ms.date: 12/05/2018
ms.keywords: IEnumOleUndoUnits interface [COM],Reset method, IEnumOleUndoUnits.Reset, IEnumOleUndoUnits::Reset, Reset, Reset method [COM], Reset method [COM],IEnumOleUndoUnits interface, _ole_ienumoleundounits_reset, com.ienumoleundounits_reset, ocidl/IEnumOleUndoUnits::Reset
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
 - IEnumOleUndoUnits::Reset
 - ocidl/IEnumOleUndoUnits::Reset
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
 - IEnumOleUndoUnits.Reset
---

# IEnumOleUndoUnits::Reset


## -description

Resets the enumeration sequence to the beginning.



## -returns

This method returns S_OK on success.

## -remarks

There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumoleundounits">IEnumOleUndoUnits</a>
