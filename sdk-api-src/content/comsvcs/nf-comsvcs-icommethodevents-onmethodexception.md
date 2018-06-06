---
UID: NF:comsvcs.IComMethodEvents.OnMethodException
title: IComMethodEvents::OnMethodException
author: windows-sdk-content
description: Generated when an object's method generates an exception.
old-location: cos\icommethodevents_onmethodexception.htm
old-project: cossdk
ms.assetid: b504a2db-0d18-42f1-8572-dc066c3e7740
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComMethodEvents interface [COM+],OnMethodException method, IComMethodEvents.OnMethodException, IComMethodEvents::OnMethodException, OnMethodException, OnMethodException method [COM+], OnMethodException method [COM+],IComMethodEvents interface, _dtc_IComMethodEvents_OnMethodException, comsvcs/IComMethodEvents::OnMethodException, cos.icommethodevents_onmethodexception
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
 - IComMethodEvents.OnMethodException
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComMethodEvents::OnMethodException


## -description


Generated when an object's method generates an exception.


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


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/24670a23-4300-48f9-a089-dff3082cb544">IComMethodEvents</a>
 

 

