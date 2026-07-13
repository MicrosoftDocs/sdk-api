---
UID: NF:oleidl.IEnumOLEVERB.Skip
title: IEnumOLEVERB::Skip (oleidl.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumOLEVERB.Skip)
helpviewer_keywords: ["IEnumOLEVERB interface [COM]","Skip method","IEnumOLEVERB.Skip","IEnumOLEVERB::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumOLEVERB interface","_ole_ienumoleverb_skip","com.ienumoleverb_skip","oleidl/IEnumOLEVERB::Skip"]
old-location: com\ienumoleverb_skip.htm
tech.root: com
ms.assetid: f949f993-1c4c-4d42-ba23-93330f0e9967
ms.date: 12/05/2018
ms.keywords: IEnumOLEVERB interface [COM],Skip method, IEnumOLEVERB.Skip, IEnumOLEVERB::Skip, Skip, Skip method [COM], Skip method [COM],IEnumOLEVERB interface, _ole_ienumoleverb_skip, com.ienumoleverb_skip, oleidl/IEnumOLEVERB::Skip
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
 - IEnumOLEVERB::Skip
 - oleidl/IEnumOLEVERB::Skip
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
 - IEnumOLEVERB.Skip
---

# IEnumOLEVERB::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>
