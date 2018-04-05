---
UID: NF:comsvcs.IComMethodEvents.OnMethodReturn
title: IComMethodEvents::OnMethodReturn method
author: windows-driver-content
description: Generated when an object's method returns.
old-location: cos\icommethodevents_onmethodreturn.htm
old-project: cossdk
ms.assetid: ade20bfc-0b50-4663-a1d3-14e2bd0c19a1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IComMethodEvents, IComMethodEvents interface [COM+], OnMethodReturn method, IComMethodEvents::OnMethodReturn, OnMethodReturn method [COM+], OnMethodReturn method [COM+], IComMethodEvents interface, OnMethodReturn,IComMethodEvents.OnMethodReturn, _dtc_icommethodevents_onmethodreturn, comsvcs/IComMethodEvents::OnMethodReturn, cos.icommethodevents_onmethodreturn
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
-	IComMethodEvents.OnMethodReturn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComMethodEvents::OnMethodReturn method


## -description


Generated when an object's method returns.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param oid [in]

The just-in-time (JIT) activated object.


### -param guidCid [in]

The CLSID for the object being called.


### -param guidRid [in]

The identifier of the method.


### -param iMeth [in]

The v-table index of the method.


### -param hresult [in]

The result of the method call.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/24670a23-4300-48f9-a089-dff3082cb544">IComMethodEvents</a>
 

 

