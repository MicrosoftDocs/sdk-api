---
UID: NF:comsvcs.IComObjectPoolEvents.OnObjPoolGetObject
title: IComObjectPoolEvents::OnObjPoolGetObject
author: windows-sdk-content
description: Generated when a non-transactional object is obtained from the pool.
old-location: cos\icomobjectpoolevents_onobjpoolgetobject.htm
tech.root: cossdk
ms.assetid: 532575b4-af72-4b53-b90b-fc09966c8ee0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IComObjectPoolEvents interface [COM+],OnObjPoolGetObject method, IComObjectPoolEvents.OnObjPoolGetObject, IComObjectPoolEvents::OnObjPoolGetObject, OnObjPoolGetObject, OnObjPoolGetObject method [COM+], OnObjPoolGetObject method [COM+],IComObjectPoolEvents interface, _dtc_IComObjectPoolEvents_OnObjPoolGetObject, comsvcs/IComObjectPoolEvents::OnObjPoolGetObject, cos.icomobjectpoolevents_onobjpoolgetobject
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IComObjectPoolEvents.OnObjPoolGetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IComObjectPoolEvents.OnObjPoolGetObject
: 
---

# IComObjectPoolEvents::OnObjPoolGetObject


## -description


Generated when a non-transactional object is obtained from the pool.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


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




<a href="https://msdn.microsoft.com/a830b40b-a1b1-464e-b532-91cebd4e5d2f">IComObjectPoolEvents</a>
 

 

