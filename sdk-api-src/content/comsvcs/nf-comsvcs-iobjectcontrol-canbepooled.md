---
UID: NF:comsvcs.IObjectControl.CanBePooled
title: IObjectControl::CanBePooled (comsvcs.h)
description: Notifies the COM+ run-time environment whether the object can be pooled for reuse when it is deactivated.
helpviewer_keywords: ["CanBePooled","CanBePooled method [COM+]","CanBePooled method [COM+]","IObjectControl interface","IObjectControl interface [COM+]","CanBePooled method","IObjectControl.CanBePooled","IObjectControl::CanBePooled","_cos_IObjectControl_CanBePooled","comsvcs/IObjectControl::CanBePooled","cos.iobjectcontrol_canbepooled"]
old-location: cos\iobjectcontrol_canbepooled.htm
tech.root: cos
ms.assetid: 97f585f1-e9c2-4122-a5e9-0a10b874b06e
ms.date: 12/05/2018
ms.keywords: CanBePooled, CanBePooled method [COM+], CanBePooled method [COM+],IObjectControl interface, IObjectControl interface [COM+],CanBePooled method, IObjectControl.CanBePooled, IObjectControl::CanBePooled, _cos_IObjectControl_CanBePooled, comsvcs/IObjectControl::CanBePooled, cos.iobjectcontrol_canbepooled
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectControl::CanBePooled
 - comsvcs/IObjectControl::CanBePooled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectControl.CanBePooled
---

# IObjectControl::CanBePooled


## -description

Notifies the COM+ run-time environment whether the object can be pooled for reuse when it is deactivated.



## -returns

If the object can be pooled for reuse, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -remarks

When an object returns <b>TRUE</b> from the <b>CanBePooled</b> method, it indicates to the COM+ run-time environment that it can be added to an object pool after deactivation rather than being destroyed. Whenever an instance is required, one is drawn from the pool rather than created.



Returning <b>TRUE</b> from the <b>CanBePooled</b> method does not guarantee that objects will be recycled; it only gives the COM+ run-time environment permission to recycle them. Returning <b>FALSE</b> from the <b>CanBePooled</b> method guarantees that instances of a component are not recycled.

The <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-activate">Activate</a> method is called if a new instance is created or if a recycled instance is drawn from the pool. Similarly, the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-deactivate">Deactivate</a> method is called every time the object is deactivated, whether it is being destroyed or returned to the pool for recycling.

## -see-also

<a href="/windows/desktop/cossdk/com--object-pooling">COM+ Object Pooling</a>



<a href="/windows/desktop/cossdk/how-object-pooling-works">How Object Pooling Works</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a>



<a href="/windows/desktop/cossdk/requirements-for-poolable-objects">Requirements for Poolable Objects</a>
