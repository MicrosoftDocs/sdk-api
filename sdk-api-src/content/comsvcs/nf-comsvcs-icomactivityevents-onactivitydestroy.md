---
UID: NF:comsvcs.IComActivityEvents.OnActivityDestroy
title: IComActivityEvents::OnActivityDestroy
author: windows-sdk-content
description: Generated when an activity is finished.
old-location: cos\icomactivityevents_onactivitydestroy.htm
old-project: cossdk
ms.assetid: af69bcf7-a925-42e2-a7a8-4ebf745955b9
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityDestroy method, IComActivityEvents.OnActivityDestroy, IComActivityEvents::OnActivityDestroy, OnActivityDestroy, OnActivityDestroy method [COM+], OnActivityDestroy method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityDestroy, comsvcs/IComActivityEvents::OnActivityDestroy, cos.icomactivityevents_onactivitydestroy
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
 - IComActivityEvents.OnActivityDestroy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComActivityEvents::OnActivityDestroy


## -description


Generated when an activity is finished.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The GUID associated with the current activity.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/9b702bcd-d5a6-41fa-98ce-00a245dfe770">IComActivityEvents</a>
 

 

