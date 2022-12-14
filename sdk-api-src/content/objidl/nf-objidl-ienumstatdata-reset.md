---
UID: NF:objidl.IEnumSTATDATA.Reset
title: IEnumSTATDATA::Reset (objidl.h)
description: Resets the enumeration sequence to the beginning. (IEnumSTATDATA.Reset)
helpviewer_keywords: ["IEnumSTATDATA interface [COM]","Reset method","IEnumSTATDATA.Reset","IEnumSTATDATA::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumSTATDATA interface","_ole_ienumstatdata_reset","com.ienumstatdata_reset","objidl/IEnumSTATDATA::Reset"]
old-location: com\ienumstatdata_reset.htm
tech.root: com
ms.assetid: 239edaf7-9e4c-4652-a2d8-08b798ed22ee
ms.date: 12/05/2018
ms.keywords: IEnumSTATDATA interface [COM],Reset method, IEnumSTATDATA.Reset, IEnumSTATDATA::Reset, Reset, Reset method [COM], Reset method [COM],IEnumSTATDATA interface, _ole_ienumstatdata_reset, com.ienumstatdata_reset, objidl/IEnumSTATDATA::Reset
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
 - IEnumSTATDATA::Reset
 - objidl/IEnumSTATDATA::Reset
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
 - IEnumSTATDATA.Reset
---

# IEnumSTATDATA::Reset


## -description

Resets the enumeration sequence to the beginning.



## -returns

This method returns S_OK on success.

## -remarks

There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>
