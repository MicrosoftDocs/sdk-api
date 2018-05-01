---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolCreatePool
title: IComObjectPoolEvents2::OnObjPoolCreatePool method
author: windows-driver-content
description: Generated when a new pool is created.
old-location: cos\icomobjectpoolevents2_onobjpoolcreatepool.htm
old-project: cossdk
ms.assetid: fa7a5ee4-8304-426c-9063-d25e2ed69668
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComObjectPoolEvents2, IComObjectPoolEvents2 interface [COM+], OnObjPoolCreatePool method, IComObjectPoolEvents2::OnObjPoolCreatePool, OnObjPoolCreatePool method [COM+], OnObjPoolCreatePool method [COM+], IComObjectPoolEvents2 interface, OnObjPoolCreatePool,IComObjectPoolEvents2.OnObjPoolCreatePool, _dtc_IComObjectPoolEvents2_OnObjPoolCreatePool, comsvcs/IComObjectPoolEvents2::OnObjPoolCreatePool, cos.icomobjectpoolevents2_onobjpoolcreatepool
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
-	IComObjectPoolEvents2.OnObjPoolCreatePool
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPoolEvents2::OnObjPoolCreatePool method


## -description


Generated when a new pool is created.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param dwMin [in]

The pool's minimum object value.


### -param dwMax [in]

The pool's maximum object value.


### -param dwTimeout [in]

The pool's time-out value.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f1891d8b-e3d0-4378-ac67-c2c0ddd65602">IComObjectPoolEvents2</a>
 

 

