---
UID: NF:ocidl.IEnumConnections.Clone
title: IEnumConnections::Clone (ocidl.h)

description: Creates a new enumerator that contains the same enumeration state as the current one.
old-location: com\ienumconnections_clone.htm
tech.root: com
ms.assetid: 00edeff3-a2e4-4e25-8771-32e3e4353274

ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumConnections interface, IEnumConnections interface [COM],Clone method, IEnumConnections.Clone, IEnumConnections::Clone, _com_ienumconnections_clone, com.ienumconnections_clone, ocidl/IEnumConnections::Clone
ms.topic: method
f1_keywords: 
 - "ocidl/IEnumConnections.Clone"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ocidl.h
api_name:
 - IEnumConnections.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumConnections::Clone


## -description


Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.


## -parameters




### -param ppEnum [out]

A pointer to the cloned enumerator object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
 

 

