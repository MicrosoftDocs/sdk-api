---
UID: NF:comsvcs.IComObjectPool2Events.OnObjPoolGetFromTx2
title: IComObjectPool2Events::OnObjPoolGetFromTx2
author: windows-driver-content
description: Generated when a transactional object is obtained from the pool.
old-location: cos\icomobjectpool2events_onobjpoolgetfromtx2.htm
old-project: cossdk
ms.assetid: d1c8b02a-8262-48f6-a160-5bef21bed5ce
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IComObjectPool2Events interface [COM+],OnObjPoolGetFromTx2 method, IComObjectPool2Events.OnObjPoolGetFromTx2, IComObjectPool2Events::OnObjPoolGetFromTx2, OnObjPoolGetFromTx2, OnObjPoolGetFromTx2 method [COM+], OnObjPoolGetFromTx2 method [COM+],IComObjectPool2Events interface, _dtc_IComObjectPool2Events_OnObjPoolGetFromTx2, comsvcs/IComObjectPool2Events::OnObjPoolGetFromTx2, cos.icomobjectpool2events_onobjpoolgetfromtx2
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
-	IComObjectPool2Events.OnObjPoolGetFromTx2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPool2Events::OnObjPoolGetFromTx2


## -description


Generated when a transactional object is obtained from the pool.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The activity ID for which the object is created.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param guidTx [in]

The GUID representing the transaction identifier.


### -param objid [in]

The unique identifier for this object.


### -param guidPartition [in]

The partition identifier for this instance.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/2aac494d-52ce-408c-8444-8792b5b53604">IComObjectPool2Events</a>
 

 

