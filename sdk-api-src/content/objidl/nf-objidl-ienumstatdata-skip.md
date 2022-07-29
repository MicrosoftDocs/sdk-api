---
UID: NF:objidl.IEnumSTATDATA.Skip
title: IEnumSTATDATA::Skip (objidl.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumSTATDATA.Skip)
helpviewer_keywords: ["IEnumSTATDATA interface [COM]","Skip method","IEnumSTATDATA.Skip","IEnumSTATDATA::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumSTATDATA interface","_ole_ienumstatdata_skip","com.ienumstatdata_skip","objidl/IEnumSTATDATA::Skip"]
old-location: com\ienumstatdata_skip.htm
tech.root: com
ms.assetid: fe3d45bc-bdcf-4e05-a03f-a40780b016e4
ms.date: 12/05/2018
ms.keywords: IEnumSTATDATA interface [COM],Skip method, IEnumSTATDATA.Skip, IEnumSTATDATA::Skip, Skip, Skip method [COM], Skip method [COM],IEnumSTATDATA interface, _ole_ienumstatdata_skip, com.ienumstatdata_skip, objidl/IEnumSTATDATA::Skip
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
 - IEnumSTATDATA::Skip
 - objidl/IEnumSTATDATA::Skip
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
 - IEnumSTATDATA.Skip
---

# IEnumSTATDATA::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>
