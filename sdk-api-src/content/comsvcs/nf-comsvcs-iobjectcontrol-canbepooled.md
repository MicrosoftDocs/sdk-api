---
UID: NF:comsvcs.IObjectControl.CanBePooled
title: IObjectControl::CanBePooled (comsvcs.h)
author: windows-sdk-content
description: Notifies the COM+ run-time environment whether the object can be pooled for reuse when it is deactivated.
old-location: cos\iobjectcontrol_canbepooled.htm
tech.root: cossdk
ms.assetid: 97f585f1-e9c2-4122-a5e9-0a10b874b06e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CanBePooled, CanBePooled method [COM+], CanBePooled method [COM+],IObjectControl interface, IObjectControl interface [COM+],CanBePooled method, IObjectControl.CanBePooled, IObjectControl::CanBePooled, _cos_IObjectControl_CanBePooled, comsvcs/IObjectControl::CanBePooled, cos.iobjectcontrol_canbepooled
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectControl.CanBePooled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectControl::CanBePooled


## -description


Notifies the COM+ run-time environment whether the object can be pooled for reuse when it is deactivated.


## -parameters






## -returns



If the object can be pooled for reuse, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.




## -remarks



When an object returns <b>TRUE</b> from the <b>CanBePooled</b> method, it indicates to the COM+ run-time environment that it can be added to an object pool after deactivation rather than being destroyed. Whenever an instance is required, one is drawn from the pool rather than created.



Returning <b>TRUE</b> from the <b>CanBePooled</b> method does not guarantee that objects will be recycled; it only gives the COM+ run-time environment permission to recycle them. Returning <b>FALSE</b> from the <b>CanBePooled</b> method guarantees that instances of a component are not recycled.

The <a href="https://msdn.microsoft.com/53bf55a2-0cfa-4612-bca7-c6693f84e18f">Activate</a> method is called if a new instance is created or if a recycled instance is drawn from the pool. Similarly, the <a href="https://msdn.microsoft.com/e076e7ce-867a-47ab-bd7e-9754b7d81e43">Deactivate</a> method is called every time the object is deactivated, whether it is being destroyed or returned to the pool for recycling.





## -see-also




<a href="https://msdn.microsoft.com/954cf9ee-e76c-4faf-99aa-3648a7bb8a59">COM+ Object Pooling</a>



<a href="https://msdn.microsoft.com/34978b50-cd20-42fd-ad46-410190478ef8">How Object Pooling Works</a>



<a href="https://msdn.microsoft.com/cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4">IObjectControl</a>



<a href="https://msdn.microsoft.com/2cd4211e-be12-4197-8b43-5cb9f2321016">Requirements for Poolable Objects</a>
 

 

