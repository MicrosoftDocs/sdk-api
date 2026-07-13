---
UID: NF:comsvcs.IComObjectPool2Events.OnObjPoolGetObject2
title: IComObjectPool2Events::OnObjPoolGetObject2 (comsvcs.h)
description: Generated when a non-transactional object is obtained from the pool. (IComObjectPool2Events.OnObjPoolGetObject2)
helpviewer_keywords: ["IComObjectPool2Events interface [COM+]","OnObjPoolGetObject2 method","IComObjectPool2Events.OnObjPoolGetObject2","IComObjectPool2Events::OnObjPoolGetObject2","OnObjPoolGetObject2","OnObjPoolGetObject2 method [COM+]","OnObjPoolGetObject2 method [COM+]","IComObjectPool2Events interface","_dtc_IComObjectPool2Events_OnObjPoolGetObject2","comsvcs/IComObjectPool2Events::OnObjPoolGetObject2","cos.icomobjectpool2events_onobjpoolgetobject2"]
old-location: cos\icomobjectpool2events_onobjpoolgetobject2.htm
tech.root: cos
ms.assetid: 322540f2-7f99-41ad-b6b5-59067f350feb
ms.date: 12/05/2018
ms.keywords: IComObjectPool2Events interface [COM+],OnObjPoolGetObject2 method, IComObjectPool2Events.OnObjPoolGetObject2, IComObjectPool2Events::OnObjPoolGetObject2, OnObjPoolGetObject2, OnObjPoolGetObject2 method [COM+], OnObjPoolGetObject2 method [COM+],IComObjectPool2Events interface, _dtc_IComObjectPool2Events_OnObjPoolGetObject2, comsvcs/IComObjectPool2Events::OnObjPoolGetObject2, cos.icomobjectpool2events_onobjpoolgetobject2
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
 - IComObjectPool2Events::OnObjPoolGetObject2
 - comsvcs/IComObjectPool2Events::OnObjPoolGetObject2
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
 - IComObjectPool2Events.OnObjPoolGetObject2
---

# IComObjectPool2Events::OnObjPoolGetObject2


## -description

Generated when a non-transactional object is obtained from the pool.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidActivity [in]

The activity ID for which the object is created.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param dwAvailable [in]

The number of objects in the pool.

### -param oid [in]

The unique identifier for this object.

### -param guidPartition [in]

The partition identifier for this instance.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpool2events">IComObjectPool2Events</a>
