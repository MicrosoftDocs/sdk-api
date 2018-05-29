---
UID: NF:comsvcs.IComObjectPool2Events.OnObjPoolPutObject2
title: IComObjectPool2Events::OnObjPoolPutObject2
author: windows-sdk-content
description: Generated when an object is added to the pool.
old-location: cos\icomobjectpool2events_onobjpoolputobject2.htm
old-project: cossdk
ms.assetid: 5a0cfbd2-d88c-4773-96e5-0e97767d647d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComObjectPool2Events interface [COM+],OnObjPoolPutObject2 method, IComObjectPool2Events.OnObjPoolPutObject2, IComObjectPool2Events::OnObjPoolPutObject2, OnObjPoolPutObject2, OnObjPoolPutObject2 method [COM+], OnObjPoolPutObject2 method [COM+],IComObjectPool2Events interface, _dtc_IComObjectPool2Events_OnObjPoolPutObject2, comsvcs/IComObjectPool2Events::OnObjPoolPutObject2, cos.icomobjectpool2events_onobjpoolputobject2
ms.prod: windows
ms.technology: windows-sdk
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
-	IComObjectPool2Events.OnObjPoolPutObject2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPool2Events::OnObjPoolPutObject2


## -description


Generated when an object is added to the pool.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


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




<a href="https://msdn.microsoft.com/2aac494d-52ce-408c-8444-8792b5b53604">IComObjectPool2Events</a>
 

 

