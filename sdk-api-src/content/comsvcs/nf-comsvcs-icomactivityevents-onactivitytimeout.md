---
UID: NF:comsvcs.IComActivityEvents.OnActivityTimeout
title: IComActivityEvents::OnActivityTimeout
author: windows-sdk-content
description: Generated when a call into an activity times out.
old-location: cos\icomactivityevents_onactivitytimeout.htm
old-project: cossdk
ms.assetid: f097bea7-99a4-41eb-9518-834683d9402b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityTimeout method, IComActivityEvents.OnActivityTimeout, IComActivityEvents::OnActivityTimeout, OnActivityTimeout, OnActivityTimeout method [COM+], OnActivityTimeout method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityTimeout, comsvcs/IComActivityEvents::OnActivityTimeout, cos.icomactivityevents_onactivitytimeout
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
 - IComActivityEvents.OnActivityTimeout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComActivityEvents::OnActivityTimeout


## -description


Generated when a call into an activity times out.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidCurrent [in]

The GUID associated with the current activity.


### -param guidEntered [in]

The causality identifier for the caller.


### -param dwThread [in]

The identifier of the  thread executing the call.


### -param dwTimeout [in]

The time-out period.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/9b702bcd-d5a6-41fa-98ce-00a245dfe770">IComActivityEvents</a>
 

 

