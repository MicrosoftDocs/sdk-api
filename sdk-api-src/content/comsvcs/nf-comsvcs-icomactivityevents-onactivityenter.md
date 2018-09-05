---
UID: NF:comsvcs.IComActivityEvents.OnActivityEnter
title: IComActivityEvents::OnActivityEnter
author: windows-sdk-content
description: Generated when an activity thread is entered.
old-location: cos\icomactivityevents_onactivityenter.htm
old-project: cossdk
ms.assetid: 5933798d-2208-4eab-8024-50236e5483a3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityEnter method, IComActivityEvents.OnActivityEnter, IComActivityEvents::OnActivityEnter, OnActivityEnter, OnActivityEnter method [COM+], OnActivityEnter method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityEnter, comsvcs/IComActivityEvents::OnActivityEnter, cos.icomactivityevents_onactivityenter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
 - IComActivityEvents.OnActivityEnter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComActivityEvents::OnActivityEnter


## -description


Generated when an activity thread is entered.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidCurrent [in]

The GUID associated with the caller.


### -param guidEntered [in]

The GUID associated with the activity thread entered.


### -param dwThread [in]

The identifier of the activity thread.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/9b702bcd-d5a6-41fa-98ce-00a245dfe770">IComActivityEvents</a>
 

 

