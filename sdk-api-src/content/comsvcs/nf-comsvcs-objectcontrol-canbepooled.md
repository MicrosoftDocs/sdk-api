---
UID: NF:comsvcs.ObjectControl.CanBePooled
title: ObjectControl::CanBePooled (comsvcs.h)
author: windows-sdk-content
description: Indicates whether the object can be pooled for reuse when it is deactivated.
old-location: cos\objectcontrol_canbepooled.htm
tech.root: cossdk
ms.assetid: 1bca2892-4b9a-4135-b009-37181a028130
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CanBePooled, CanBePooled method [COM+], CanBePooled method [COM+],ObjectControl interface, ObjectControl interface [COM+],CanBePooled method, ObjectControl.CanBePooled, ObjectControl::CanBePooled, _cos_ObjectControl_CanBePooled, comsvcs/ObjectControl::CanBePooled, cos.objectcontrol_canbepooled
ms.topic: method
f1_keywords: 
 - "comsvcs/ObjectControl.CanBePooled"
dev_langs:
 - c++
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
 - ObjectControl.CanBePooled
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontrol-activate">Activate</a> method is called if a new instance is created or if a recycled instance is drawn from the pool. Similarly, the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontrol-deactivate">Deactivate</a> method is called every time the object is deactivated, whether it is being destroyed or returned to the pool for recycling.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--object-pooling">COM+ Object Pooling</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/how-object-pooling-works">How Object Pooling Works</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-objectcontrol">ObjectControl</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/requirements-for-poolable-objects">Requirements for Poolable Objects</a>
 

 

