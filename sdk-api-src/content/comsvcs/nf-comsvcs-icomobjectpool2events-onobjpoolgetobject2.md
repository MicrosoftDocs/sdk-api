---
UID: NF:comsvcs.IComObjectPool2Events.OnObjPoolGetObject2
title: IComObjectPool2Events::OnObjPoolGetObject2
author: windows-driver-content
description: Generated when a non-transactional object is obtained from the pool.
old-location: cos\icomobjectpool2events_onobjpoolgetobject2.htm
old-project: cossdk
ms.assetid: 322540f2-7f99-41ad-b6b5-59067f350feb
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IComObjectPool2Events interface [COM+],OnObjPoolGetObject2 method, IComObjectPool2Events.OnObjPoolGetObject2, IComObjectPool2Events::OnObjPoolGetObject2, OnObjPoolGetObject2, OnObjPoolGetObject2 method [COM+], OnObjPoolGetObject2 method [COM+],IComObjectPool2Events interface, _dtc_IComObjectPool2Events_OnObjPoolGetObject2, comsvcs/IComObjectPool2Events::OnObjPoolGetObject2, cos.icomobjectpool2events_onobjpoolgetobject2
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComObjectPool2Events.OnObjPoolGetObject2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPool2Events::OnObjPoolGetObject2


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


### -param guidPartition [in]

The partition identifier for this instance.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/2aac494d-52ce-408c-8444-8792b5b53604">IComObjectPool2Events</a>
 

 

