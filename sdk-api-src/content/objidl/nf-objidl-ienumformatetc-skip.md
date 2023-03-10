---
UID: NF:objidl.IEnumFORMATETC.Skip
title: IEnumFORMATETC::Skip (objidl.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumFORMATETC.Skip)
helpviewer_keywords: ["IEnumFORMATETC interface [COM]","Skip method","IEnumFORMATETC.Skip","IEnumFORMATETC::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumFORMATETC interface","_ole_ienumformatetc_skip","com.ienumformatetc_skip","objidl/IEnumFORMATETC::Skip"]
old-location: com\ienumformatetc_skip.htm
tech.root: com
ms.assetid: 5fdf81ee-df31-4702-8b5e-f540ca3e6602
ms.date: 12/05/2018
ms.keywords: IEnumFORMATETC interface [COM],Skip method, IEnumFORMATETC.Skip, IEnumFORMATETC::Skip, Skip, Skip method [COM], Skip method [COM],IEnumFORMATETC interface, _ole_ienumformatetc_skip, com.ienumformatetc_skip, objidl/IEnumFORMATETC::Skip
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
 - IEnumFORMATETC::Skip
 - objidl/IEnumFORMATETC::Skip
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
 - IEnumFORMATETC.Skip
---

# IEnumFORMATETC::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>
