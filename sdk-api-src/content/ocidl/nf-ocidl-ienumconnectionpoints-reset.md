---
UID: NF:ocidl.IEnumConnectionPoints.Reset
title: IEnumConnectionPoints::Reset (ocidl.h)
description: Resets the enumeration sequence to the beginning. (IEnumConnectionPoints.Reset)
helpviewer_keywords: ["IEnumConnectionPoints interface [COM]","Reset method","IEnumConnectionPoints.Reset","IEnumConnectionPoints::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumConnectionPoints interface","_com_ienumconnectionpoints_reset","com.ienumconnectionpoints_reset","ocidl/IEnumConnectionPoints::Reset"]
old-location: com\ienumconnectionpoints_reset.htm
tech.root: com
ms.assetid: a3624bf7-c56c-4ae6-9bc4-2490ddf02171
ms.date: 12/05/2018
ms.keywords: IEnumConnectionPoints interface [COM],Reset method, IEnumConnectionPoints.Reset, IEnumConnectionPoints::Reset, Reset, Reset method [COM], Reset method [COM],IEnumConnectionPoints interface, _com_ienumconnectionpoints_reset, com.ienumconnectionpoints_reset, ocidl/IEnumConnectionPoints::Reset
req.header: ocidl.h
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
 - IEnumConnectionPoints::Reset
 - ocidl/IEnumConnectionPoints::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ocidl.h
api_name:
 - IEnumConnectionPoints.Reset
---

# IEnumConnectionPoints::Reset


## -description

Resets the enumeration sequence to the beginning.



## -returns

The return value is S_OK.

## -remarks

There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>
