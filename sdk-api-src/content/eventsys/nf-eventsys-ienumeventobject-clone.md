---
UID: NF:eventsys.IEnumEventObject.Clone
title: IEnumEventObject::Clone method
author: windows-driver-content
description: Creates an enumerator that contains the same enumeration state as the current one.
old-location: cos\ienumeventobject_clone.htm
old-project: cossdk
ms.assetid: 25bd3f8f-ba99-42e6-b7af-6b237343a17c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Clone method [COM+], Clone method [COM+], IEnumEventObject interface, Clone,IEnumEventObject.Clone, IEnumEventObject, IEnumEventObject interface [COM+], Clone method, IEnumEventObject::Clone, _cos_ienumeventobject_clone, cos.ienumeventobject_clone, eventsys/IEnumEventObject::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Eventsys.h
api_name:
-	IEnumEventObject.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnumEventObject::Clone method


## -description


Creates an enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppInterface [out]

Address of a pointer to the <a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a> interface on the enumeration object. This parameter cannot be <b>NULL</b>. If the method is unsuccessful, the value of this output variable is undefined.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



When the pointer to the <a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a> is returned, it is positioned at the first object in the collection not at the place of the enumeration object being cloned.




## -see-also




<a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a>
 

 

