---
UID: NF:comsvcs.IComActivityEvents.OnActivityLeave
title: IComActivityEvents::OnActivityLeave method
author: windows-driver-content
description: Generated when an activity thread is left.
old-location: cos\icomactivityevents_onactivityleave.htm
old-project: cossdk
ms.assetid: f39a8ce1-9c17-47eb-9405-c6a69dee88cc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IComActivityEvents, IComActivityEvents interface [COM+], OnActivityLeave method, IComActivityEvents::OnActivityLeave, OnActivityLeave method [COM+], OnActivityLeave method [COM+], IComActivityEvents interface, OnActivityLeave,IComActivityEvents.OnActivityLeave, _dtc_IComActivityEvents_OnActivityLeave, comsvcs/IComActivityEvents::OnActivityLeave, cos.icomactivityevents_onactivityleave
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
-	IComActivityEvents.OnActivityLeave
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComActivityEvents::OnActivityLeave method


## -description


Generated when an activity thread is left.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidCurrent [in]

The GUID associated with the caller.


### -param guidLeft [in]

The GUID associated with the activity thread left.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/9b702bcd-d5a6-41fa-98ce-00a245dfe770">IComActivityEvents</a>
 

 

