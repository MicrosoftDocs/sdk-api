---
UID: NF:comsvcs.IComThreadEvents.OnThreadAssignApartment
title: IComThreadEvents::OnThreadAssignApartment
author: windows-driver-content
description: Generated when an activity is assigned to an apartment thread.
old-location: cos\icomthreadevents_onthreadassignapartment.htm
old-project: cossdk
ms.assetid: 2711b4b9-f27c-42c4-8f78-f31ffba2cfcf
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadAssignApartment method, IComThreadEvents.OnThreadAssignApartment, IComThreadEvents::OnThreadAssignApartment, OnThreadAssignApartment, OnThreadAssignApartment method [COM+], OnThreadAssignApartment method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadAssignApartment, comsvcs/IComThreadEvents::OnThreadAssignApartment, cos.icomthreadevents_onthreadassignapartment
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
-	IComThreadEvents.OnThreadAssignApartment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComThreadEvents::OnThreadAssignApartment


## -description


Generated when an activity is assigned to an apartment thread.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The activity identifier for which the object is created.


### -param AptID [in]

The apartment identifier.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/a6523088-cca4-41c1-a3fe-d8cb7320ff33">IComThreadEvents</a>
 

 

