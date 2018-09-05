---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolCreateDecision
title: IComObjectPoolEvents2::OnObjPoolCreateDecision
author: windows-sdk-content
description: Generated when a pool provides a requesting client with an existing object or creates a new one.
old-location: cos\icomobjectpoolevents2_onobjpoolcreatedecision.htm
old-project: cossdk
ms.assetid: a66c00ac-b9b9-431e-b1c8-6642cb35ec3c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolCreateDecision method, IComObjectPoolEvents2.OnObjPoolCreateDecision, IComObjectPoolEvents2::OnObjPoolCreateDecision, OnObjPoolCreateDecision, OnObjPoolCreateDecision method [COM+], OnObjPoolCreateDecision method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolCreateDecision, comsvcs/IComObjectPoolEvents2::OnObjPoolCreateDecision, cos.icomobjectpoolevents2_onobjpoolcreatedecision
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComObjectPoolEvents2.OnObjPoolCreateDecision
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPoolEvents2::OnObjPoolCreateDecision


## -description


Generated when a pool provides a requesting client with an existing object or creates a new one.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param dwThreadsWaiting [in]

The number of threads waiting for an object.


### -param dwAvail [in]

The number of free objects in the pool.


### -param dwCreated [in]

The number of total objects in the pool.


### -param dwMin [in]

The pool's minimum object value.


### -param dwMax [in]

The pool's maximum object value.


## -returns



The user verifies the return values from this method.




## -remarks



When a component is configured for object pooling, the pool is populated with objects up to the specified minimum level. As client requests for the component come in, they are satisfied on a first-come first-served basis from the pool. If no pooled objects are available and the pool is not yet at its specified maximum level, a new object is created and activated for the client.




## -see-also




<a href="https://msdn.microsoft.com/f1891d8b-e3d0-4378-ac67-c2c0ddd65602">IComObjectPoolEvents2</a>
 

 

