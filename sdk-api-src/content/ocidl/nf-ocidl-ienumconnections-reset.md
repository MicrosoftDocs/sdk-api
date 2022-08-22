---
UID: NF:ocidl.IEnumConnections.Reset
title: IEnumConnections::Reset (ocidl.h)
description: Resets the enumeration sequence to the beginning. (IEnumConnections.Reset)
helpviewer_keywords: ["IEnumConnections interface [COM]","Reset method","IEnumConnections.Reset","IEnumConnections::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumConnections interface","_com_ienumconnections_reset","com.ienumconnections_reset","ocidl/IEnumConnections::Reset"]
old-location: com\ienumconnections_reset.htm
tech.root: com
ms.assetid: 444c9398-199f-4d87-9b1e-075d5af0b649
ms.date: 12/05/2018
ms.keywords: IEnumConnections interface [COM],Reset method, IEnumConnections.Reset, IEnumConnections::Reset, Reset, Reset method [COM], Reset method [COM],IEnumConnections interface, _com_ienumconnections_reset, com.ienumconnections_reset, ocidl/IEnumConnections::Reset
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
 - IEnumConnections::Reset
 - ocidl/IEnumConnections::Reset
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
 - IEnumConnections.Reset
---

# IEnumConnections::Reset


## -description

Resets the enumeration sequence to the beginning.



## -returns

The return value is S_OK.

## -remarks

There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
