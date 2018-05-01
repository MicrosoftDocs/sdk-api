---
UID: NF:objidl.IEnumContextProps.Next
title: IEnumContextProps::Next method
author: windows-driver-content
description: Retrieves the specified number of items in the enumeration sequence.
old-location: com\ienumcontextprops_next.htm
old-project: com
ms.assetid: d1856f5c-dfed-462c-aca3-91b7973d6d8d
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IEnumContextProps, IEnumContextProps interface [COM], Next method, IEnumContextProps::Next, Next method [COM], Next method [COM], IEnumContextProps interface, Next,IEnumContextProps.Next, _com_ienumcontextprops_next, com.ienumcontextprops_next, objidlbase/IEnumContextProps::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IEnumContextProps.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumContextProps::Next method


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.


### -param pContextProperties [out]

An array of enumerated items.

The enumerator is responsible for allocating any memory, and the caller is responsible for freeing it. If <i>celt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pceltFetched</i> to know how many pointers to release.


### -param pceltFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.


## -returns



If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/64591e45-5478-4360-8c1f-08b09b5aef8e">IEnumContextProps</a>
 

 

