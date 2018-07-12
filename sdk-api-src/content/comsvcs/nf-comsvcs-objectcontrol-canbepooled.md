---
UID: NF:comsvcs.ObjectControl.CanBePooled
title: ObjectControl::CanBePooled
author: windows-sdk-content
description: Indicates whether the object can be pooled for reuse when it is deactivated.
old-location: cos\objectcontrol_canbepooled.htm
old-project: cossdk
ms.assetid: 1bca2892-4b9a-4135-b009-37181a028130
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: CanBePooled, CanBePooled method [COM+], CanBePooled method [COM+],ObjectControl interface, ObjectControl interface [COM+],CanBePooled method, ObjectControl.CanBePooled, ObjectControl::CanBePooled, _cos_ObjectControl_CanBePooled, comsvcs/ObjectControl::CanBePooled, cos.objectcontrol_canbepooled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ObjectControl.CanBePooled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ObjectControl::CanBePooled


## -description


Indicates whether the object can be pooled for reuse when it is deactivated.


## -parameters




### -param pbPoolable [out]

Indicates whether the COM+ run-time environment can pool this object on deactivation for later reuse.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



When an object returns <b>TRUE</b> from <b>CanBePooled</b>, it indicates to the COM+ run-time environment that it can be added to an object pool after deactivation rather than being destroyed. Whenever an instance is required, one is drawn from the pool rather than being created.

Returning <b>TRUE</b> from <b>CanBePooled</b> does not guarantee that objects will be recycled; it only gives the COM+ run-time environment permission to recycle them. Returning <b>FALSE</b> from the <b>CanBePooled</b> method guarantees that instances of a component are not recycled.

The <a href="https://msdn.microsoft.com/70b260e7-a51d-4ddc-b395-5478e368e776">Activate</a> method is called if a new instance is created or if a recycled instance is drawn from the pool. Similarly, the <a href="https://msdn.microsoft.com/86ab7f50-6f2e-4c6c-ba4d-fd302cccf97d">Deactivate</a> method is called every time the object is deactivated, whether it is being destroyed or returned to the pool for recycling.




## -see-also




<a href="https://msdn.microsoft.com/954cf9ee-e76c-4faf-99aa-3648a7bb8a59">COM+ Object Pooling</a>



<a href="https://msdn.microsoft.com/34978b50-cd20-42fd-ad46-410190478ef8">How Object Pooling Works</a>



<a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a>



<a href="https://msdn.microsoft.com/2cd4211e-be12-4197-8b43-5cb9f2321016">Requirements for Poolable Objects</a>
 

 

