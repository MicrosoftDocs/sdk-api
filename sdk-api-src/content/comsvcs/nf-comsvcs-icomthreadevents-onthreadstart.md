---
UID: NF:comsvcs.IComThreadEvents.OnThreadStart
title: IComThreadEvents::OnThreadStart method
author: windows-driver-content
description: Generated when a single-threaded apartment (STA) thread is started.
old-location: cos\icomthreadevents_onthreadstart.htm
old-project: cossdk
ms.assetid: 9316965e-13e8-4e3a-9404-8e49334773bc
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComThreadEvents, IComThreadEvents interface [COM+], OnThreadStart method, IComThreadEvents::OnThreadStart, OnThreadStart method [COM+], OnThreadStart method [COM+], IComThreadEvents interface, OnThreadStart,IComThreadEvents.OnThreadStart, _dtc_IComThreadEvents_OnThreadStart, comsvcs/IComThreadEvents::OnThreadStart, cos.icomthreadevents_onthreadstart
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
-	IComThreadEvents.OnThreadStart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComThreadEvents::OnThreadStart method


## -description


Generated when a single-threaded apartment (STA) thread is started.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ThreadID [in]

The unique thread identifier.


### -param dwThread [in]

The Windows thread identifier.


### -param dwTheadCnt [in]

The number of threads in the STA thread pool.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/a6523088-cca4-41c1-a3fe-d8cb7320ff33">IComThreadEvents</a>
 

 

