---
UID: NF:objidl.IEnumFORMATETC.Reset
title: IEnumFORMATETC::Reset (objidl.h)
description: Resets the enumeration sequence to the beginning. (IEnumFORMATETC.Reset)
helpviewer_keywords: ["IEnumFORMATETC interface [COM]","Reset method","IEnumFORMATETC.Reset","IEnumFORMATETC::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumFORMATETC interface","_ole_ienumformatetc_reset","com.ienumformatetc_reset","objidl/IEnumFORMATETC::Reset"]
old-location: com\ienumformatetc_reset.htm
tech.root: com
ms.assetid: f079c166-c4a8-4827-a8c5-3c5e0cb13b77
ms.date: 12/05/2018
ms.keywords: IEnumFORMATETC interface [COM],Reset method, IEnumFORMATETC.Reset, IEnumFORMATETC::Reset, Reset, Reset method [COM], Reset method [COM],IEnumFORMATETC interface, _ole_ienumformatetc_reset, com.ienumformatetc_reset, objidl/IEnumFORMATETC::Reset
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IEnumFORMATETC::Reset
 - objidl/IEnumFORMATETC::Reset
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
 - IEnumFORMATETC.Reset
---

# IEnumFORMATETC::Reset


## -description

Resets the enumeration sequence to the beginning.



## -returns

This method returns S_OK on success.

## -remarks

There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>
