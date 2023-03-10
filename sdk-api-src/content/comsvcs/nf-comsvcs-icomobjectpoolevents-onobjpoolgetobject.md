---
UID: NF:comsvcs.IComObjectPoolEvents.OnObjPoolGetObject
title: IComObjectPoolEvents::OnObjPoolGetObject (comsvcs.h)
description: Generated when a non-transactional object is obtained from the pool. (IComObjectPoolEvents.OnObjPoolGetObject)
helpviewer_keywords: ["IComObjectPoolEvents interface [COM+]","OnObjPoolGetObject method","IComObjectPoolEvents.OnObjPoolGetObject","IComObjectPoolEvents::OnObjPoolGetObject","OnObjPoolGetObject","OnObjPoolGetObject method [COM+]","OnObjPoolGetObject method [COM+]","IComObjectPoolEvents interface","_dtc_IComObjectPoolEvents_OnObjPoolGetObject","comsvcs/IComObjectPoolEvents::OnObjPoolGetObject","cos.icomobjectpoolevents_onobjpoolgetobject"]
old-location: cos\icomobjectpoolevents_onobjpoolgetobject.htm
tech.root: cos
ms.assetid: 532575b4-af72-4b53-b90b-fc09966c8ee0
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents interface [COM+],OnObjPoolGetObject method, IComObjectPoolEvents.OnObjPoolGetObject, IComObjectPoolEvents::OnObjPoolGetObject, OnObjPoolGetObject, OnObjPoolGetObject method [COM+], OnObjPoolGetObject method [COM+],IComObjectPoolEvents interface, _dtc_IComObjectPoolEvents_OnObjPoolGetObject, comsvcs/IComObjectPoolEvents::OnObjPoolGetObject, cos.icomobjectpoolevents_onobjpoolgetobject
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
 - IComObjectPoolEvents::OnObjPoolGetObject
 - comsvcs/IComObjectPoolEvents::OnObjPoolGetObject
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
 - IComObjectPoolEvents.OnObjPoolGetObject
---

# IComObjectPoolEvents::OnObjPoolGetObject


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

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents">IComObjectPoolEvents</a>
