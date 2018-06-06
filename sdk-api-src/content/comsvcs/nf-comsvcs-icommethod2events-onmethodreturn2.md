---
UID: NF:comsvcs.IComMethod2Events.OnMethodReturn2
title: IComMethod2Events::OnMethodReturn2
author: windows-sdk-content
description: Generated when an object's method returns.
old-location: cos\icommethod2events_onmethodreturn2.htm
old-project: cossdk
ms.assetid: cf5a7b69-a794-4497-99c9-20c41d454753
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComMethod2Events interface [COM+],OnMethodReturn2 method, IComMethod2Events.OnMethodReturn2, IComMethod2Events::OnMethodReturn2, OnMethodReturn2, OnMethodReturn2 method [COM+], OnMethodReturn2 method [COM+],IComMethod2Events interface, _dtc_IComMethod2Events_OnMethodReturn2, comsvcs/IComMethod2Events::OnMethodReturn2, cos.icommethod2events_onmethodreturn2
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
 - IComMethod2Events.OnMethodReturn2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComMethod2Events::OnMethodReturn2


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

The identifier of the method being called.


### -param dwThread [in]

The identifier of the thread executing the call.


### -param iMeth [in]

The v-table index of the method.


### -param hresult [in]

The result of the method call.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/e0642cb2-d5f2-4e4b-ad35-7818983ed467">IComMethod2Events</a>
 

 

