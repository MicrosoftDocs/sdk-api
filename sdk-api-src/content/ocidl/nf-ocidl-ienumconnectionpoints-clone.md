---
UID: NF:ocidl.IEnumConnectionPoints.Clone
title: IEnumConnectionPoints::Clone
author: windows-driver-content
description: Creates a new enumerator that contains the same enumeration state as the current one.
old-location: com\ienumconnectionpoints_clone.htm
old-project: com
ms.assetid: 47dfd670-57f7-4fb1-bd61-65dd4a3bc6c2
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumConnectionPoints interface, IEnumConnectionPoints interface [COM],Clone method, IEnumConnectionPoints.Clone, IEnumConnectionPoints::Clone, _com_ienumconnectionpoints_clone, com.ienumconnectionpoints_clone, ocidl/IEnumConnectionPoints::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ocidl.h
api_name:
-	IEnumConnectionPoints.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumConnectionPoints::Clone


## -description


Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.


## -parameters




### -param ppEnum [out]

A pointer to the cloned enumerator object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a>
 

 

