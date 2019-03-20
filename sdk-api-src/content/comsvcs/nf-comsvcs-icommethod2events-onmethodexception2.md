---
UID: NF:comsvcs.IComMethod2Events.OnMethodException2
title: IComMethod2Events::OnMethodException2 (comsvcs.h)
author: windows-sdk-content
description: Generated when an object's method generates an exception.
old-location: cos\icommethod2events_onmethodexception2.htm
tech.root: cossdk
ms.assetid: a797a578-2d0d-45f0-820a-2616f6c65a42
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComMethod2Events interface [COM+],OnMethodException2 method, IComMethod2Events.OnMethodException2, IComMethod2Events::OnMethodException2, OnMethodException2, OnMethodException2 method [COM+], OnMethodException2 method [COM+],IComMethod2Events interface, _dtc_IComMethod2Events_OnMethodException2, comsvcs/IComMethod2Events::OnMethodException2, cos.icommethod2events_onmethodexception2
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
 - IComMethod2Events.OnMethodException2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComMethod2Events::OnMethodException2


## -description


Generated when an object's method generates an exception.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


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


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/e0642cb2-d5f2-4e4b-ad35-7818983ed467">IComMethod2Events</a>
 

 

