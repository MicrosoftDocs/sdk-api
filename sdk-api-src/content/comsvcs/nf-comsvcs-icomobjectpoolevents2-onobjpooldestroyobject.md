---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolDestroyObject
title: IComObjectPoolEvents2::OnObjPoolDestroyObject (comsvcs.h)
description: Generated when an object is permanently removed from the pool.
helpviewer_keywords: ["IComObjectPoolEvents2 interface [COM+]","OnObjPoolDestroyObject method","IComObjectPoolEvents2.OnObjPoolDestroyObject","IComObjectPoolEvents2::OnObjPoolDestroyObject","OnObjPoolDestroyObject","OnObjPoolDestroyObject method [COM+]","OnObjPoolDestroyObject method [COM+]","IComObjectPoolEvents2 interface","_dtc_IComObjectPoolEvents2_OnObjPoolDestroyObject","comsvcs/IComObjectPoolEvents2::OnObjPoolDestroyObject","cos.icomobjectpoolevents2_onobjpooldestroyobject"]
old-location: cos\icomobjectpoolevents2_onobjpooldestroyobject.htm
tech.root: cos
ms.assetid: c942da45-4d41-4483-a30b-862d3e0c13b7
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolDestroyObject method, IComObjectPoolEvents2.OnObjPoolDestroyObject, IComObjectPoolEvents2::OnObjPoolDestroyObject, OnObjPoolDestroyObject, OnObjPoolDestroyObject method [COM+], OnObjPoolDestroyObject method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolDestroyObject, comsvcs/IComObjectPoolEvents2::OnObjPoolDestroyObject, cos.icomobjectpoolevents2_onobjpooldestroyobject
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
 - IComObjectPoolEvents2::OnObjPoolDestroyObject
 - comsvcs/IComObjectPoolEvents2::OnObjPoolDestroyObject
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
 - IComObjectPoolEvents2.OnObjPoolDestroyObject
---

# IComObjectPoolEvents2::OnObjPoolDestroyObject


## -description

Generated when an object is permanently removed from the pool.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidObject [in]

The CLSID for the objects in the pool.

### -param dwObjsCreated [in]

The number of objects in the pool.

### -param oid [in]

The unique pooled object identifier.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents2">IComObjectPoolEvents2</a>