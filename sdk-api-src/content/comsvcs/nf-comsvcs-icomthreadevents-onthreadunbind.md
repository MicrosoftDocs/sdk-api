---
UID: NF:comsvcs.IComThreadEvents.OnThreadUnBind
title: IComThreadEvents::OnThreadUnBind method
author: windows-driver-content
description: Generated when the lifetime of the configured component is over and the activity count on the apartment thread can be decremented.
old-location: cos\icomthreadevents_onthreadunbind.htm
old-project: cossdk
ms.assetid: 21ce95a4-0e87-4e2d-a3fa-b21a079058e2
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComThreadEvents, IComThreadEvents interface [COM+], OnThreadUnBind method, IComThreadEvents::OnThreadUnBind, OnThreadUnBind method [COM+], OnThreadUnBind method [COM+], IComThreadEvents interface, OnThreadUnBind,IComThreadEvents.OnThreadUnBind, _dtc_IComThreadEvents_OnThreadUnBind, comsvcs/IComThreadEvents::OnThreadUnBind, cos.icomthreadevents_onthreadunbind
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
-	IComThreadEvents.OnThreadUnBind
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComThreadEvents::OnThreadUnBind method


## -description


Generated when the lifetime of the configured component is over and the activity count on the apartment thread can be decremented.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ThreadID [in]

The unique thread identifier.


### -param AptID [in]

The apartment identifier.


### -param dwActCnt [in]

The number of current activities on the apartment thread.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/a6523088-cca4-41c1-a3fe-d8cb7320ff33">IComThreadEvents</a>
 

 

