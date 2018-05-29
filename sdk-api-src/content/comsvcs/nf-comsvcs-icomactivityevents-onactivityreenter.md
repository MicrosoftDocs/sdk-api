---
UID: NF:comsvcs.IComActivityEvents.OnActivityReenter
title: IComActivityEvents::OnActivityReenter
author: windows-sdk-content
description: Generated when an activity thread is reentered recursively.
old-location: cos\icomactivityevents_onactivityreenter.htm
old-project: cossdk
ms.assetid: e055caab-379c-47c5-b62a-28ce5c2a0573
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityReenter method, IComActivityEvents.OnActivityReenter, IComActivityEvents::OnActivityReenter, OnActivityReenter, OnActivityReenter method [COM+], OnActivityReenter method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityReenter, comsvcs/IComActivityEvents::OnActivityReenter, cos.icomactivityevents_onactivityreenter
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComActivityEvents.OnActivityReenter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComActivityEvents::OnActivityReenter


## -description


Generated when an activity thread is reentered recursively.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidCurrent [in]

The GUID associated with the caller.


### -param dwThread [in]

The identifier of the activity thread.


### -param dwCallDepth [in]

The recursion depth.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/9b702bcd-d5a6-41fa-98ce-00a245dfe770">IComActivityEvents</a>
 

 

