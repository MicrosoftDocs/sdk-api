---
UID: NF:comsvcs.IComObjectPool2Events.OnObjPoolRecycleToTx2
title: IComObjectPool2Events::OnObjPoolRecycleToTx2
author: windows-sdk-content
description: Generated when a transactional object is returned to the pool.
old-location: cos\icomobjectpool2events_onobjpoolrecycletotx2.htm
tech.root: cossdk
ms.assetid: f737289f-c990-455e-bc9b-e94f25c9297f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IComObjectPool2Events interface [COM+],OnObjPoolRecycleToTx2 method, IComObjectPool2Events.OnObjPoolRecycleToTx2, IComObjectPool2Events::OnObjPoolRecycleToTx2, OnObjPoolRecycleToTx2, OnObjPoolRecycleToTx2 method [COM+], OnObjPoolRecycleToTx2 method [COM+],IComObjectPool2Events interface, _dtc_IComObjectPool2Events_OnObjPoolRecycleToTx2, comsvcs/IComObjectPool2Events::OnObjPoolRecycleToTx2, cos.icomobjectpool2events_onobjpoolrecycletotx2
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
 - IComObjectPool2Events.OnObjPoolRecycleToTx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectPool2Events::OnObjPoolRecycleToTx2


## -description


Generated when a transactional object is returned to the pool.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The activity ID for which the object is created.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param guidTx [in]

The transaction identifier.


### -param objid [in]

The unique identifier for this object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/2aac494d-52ce-408c-8444-8792b5b53604">IComObjectPool2Events</a>
 

 

