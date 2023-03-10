---
UID: NF:comsvcs.IComObjectPoolEvents.OnObjPoolPutObject
title: IComObjectPoolEvents::OnObjPoolPutObject (comsvcs.h)
description: Generated when a new object is added to the pool.
helpviewer_keywords: ["IComObjectPoolEvents interface [COM+]","OnObjPoolPutObject method","IComObjectPoolEvents.OnObjPoolPutObject","IComObjectPoolEvents::OnObjPoolPutObject","OnObjPoolPutObject","OnObjPoolPutObject method [COM+]","OnObjPoolPutObject method [COM+]","IComObjectPoolEvents interface","_dtc_IComObjectPoolEvents_OnObjPoolPutObject","comsvcs/IComObjectPoolEvents::OnObjPoolPutObject","cos.icomobjectpoolevents_onobjpoolputobject"]
old-location: cos\icomobjectpoolevents_onobjpoolputobject.htm
tech.root: cos
ms.assetid: 00b0b3b1-943d-4fba-bd5d-52d6de80fcf6
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents interface [COM+],OnObjPoolPutObject method, IComObjectPoolEvents.OnObjPoolPutObject, IComObjectPoolEvents::OnObjPoolPutObject, OnObjPoolPutObject, OnObjPoolPutObject method [COM+], OnObjPoolPutObject method [COM+],IComObjectPoolEvents interface, _dtc_IComObjectPoolEvents_OnObjPoolPutObject, comsvcs/IComObjectPoolEvents::OnObjPoolPutObject, cos.icomobjectpoolevents_onobjpoolputobject
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
 - IComObjectPoolEvents::OnObjPoolPutObject
 - comsvcs/IComObjectPoolEvents::OnObjPoolPutObject
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
 - IComObjectPoolEvents.OnObjPoolPutObject
---

# IComObjectPoolEvents::OnObjPoolPutObject


## -description

Generated when a new object is added to the pool.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param nReason [in]

This parameter is always 0.

### -param dwAvailable [in]

The number of objects in the pool.

### -param oid [in]

The unique identifier for this object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents">IComObjectPoolEvents</a>