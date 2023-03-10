---
UID: NF:comsvcs.IComObjectPool2Events.OnObjPoolPutObject2
title: IComObjectPool2Events::OnObjPoolPutObject2 (comsvcs.h)
description: Generated when an object is added to the pool.
helpviewer_keywords: ["IComObjectPool2Events interface [COM+]","OnObjPoolPutObject2 method","IComObjectPool2Events.OnObjPoolPutObject2","IComObjectPool2Events::OnObjPoolPutObject2","OnObjPoolPutObject2","OnObjPoolPutObject2 method [COM+]","OnObjPoolPutObject2 method [COM+]","IComObjectPool2Events interface","_dtc_IComObjectPool2Events_OnObjPoolPutObject2","comsvcs/IComObjectPool2Events::OnObjPoolPutObject2","cos.icomobjectpool2events_onobjpoolputobject2"]
old-location: cos\icomobjectpool2events_onobjpoolputobject2.htm
tech.root: cos
ms.assetid: 5a0cfbd2-d88c-4773-96e5-0e97767d647d
ms.date: 12/05/2018
ms.keywords: IComObjectPool2Events interface [COM+],OnObjPoolPutObject2 method, IComObjectPool2Events.OnObjPoolPutObject2, IComObjectPool2Events::OnObjPoolPutObject2, OnObjPoolPutObject2, OnObjPoolPutObject2 method [COM+], OnObjPoolPutObject2 method [COM+],IComObjectPool2Events interface, _dtc_IComObjectPool2Events_OnObjPoolPutObject2, comsvcs/IComObjectPool2Events::OnObjPoolPutObject2, cos.icomobjectpool2events_onobjpoolputobject2
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
 - IComObjectPool2Events::OnObjPoolPutObject2
 - comsvcs/IComObjectPool2Events::OnObjPoolPutObject2
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
 - IComObjectPool2Events.OnObjPoolPutObject2
---

# IComObjectPool2Events::OnObjPoolPutObject2


## -description

Generated when an object is added to the pool.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param nReason [in]

This parameter is reserved.

### -param dwAvailable [in]

The number of objects in the pool.

### -param oid [in]

The unique identifier for this object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpool2events">IComObjectPool2Events</a>