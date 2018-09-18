---
UID: NF:objidlbase.IEnumUnknown.Clone
title: IEnumUnknown::Clone
author: windows-sdk-content
description: Creates a new enumerator that contains the same enumeration state as the current one.
old-location: com\ienumunknown_clone.htm
tech.root: com
ms.assetid: 278d2947-efa5-43c4-a950-cf39876423ba
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumUnknown interface, IEnumUnknown interface [COM],Clone method, IEnumUnknown.Clone, IEnumUnknown::Clone, _com_ienumunknown_clone, com.ienumunknown_clone, objidlbase/IEnumUnknown::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IEnumUnknown.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumUnknown::Clone


## -description


Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.


## -parameters




### -param ppenum [out]

A pointer to the cloned enumerator object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a>
 

 

