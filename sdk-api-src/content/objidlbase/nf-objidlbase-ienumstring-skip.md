---
UID: NF:objidlbase.IEnumString.Skip
title: IEnumString::Skip (objidlbase.h)
description: The IEnumString::Skip (objidlbase.h) method skips over the specified number of items in the enumeration sequence.
helpviewer_keywords: ["IEnumString interface [COM]","Skip method","IEnumString.Skip","IEnumString::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumString interface","_com_ienumstring_skip","com.ienumstring_skip","objidlbase/IEnumString::Skip"]
old-location: com\ienumstring_skip.htm
tech.root: com
ms.assetid: 8c1cd7b4-ec68-4b60-9f1e-ed01674f7f8c
ms.date: 08/13/2022
ms.keywords: IEnumString interface [COM],Skip method, IEnumString.Skip, IEnumString::Skip, Skip, Skip method [COM], Skip method [COM],IEnumString interface, _com_ienumstring_skip, com.ienumstring_skip, objidlbase/IEnumString::Skip
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
 - IEnumString::Skip
 - objidlbase/IEnumString::Skip
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
 - IEnumString.Skip
---

# IEnumString::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>
