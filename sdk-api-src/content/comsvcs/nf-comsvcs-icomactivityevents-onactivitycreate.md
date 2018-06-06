---
UID: NF:comsvcs.IComActivityEvents.OnActivityCreate
title: IComActivityEvents::OnActivityCreate
author: windows-sdk-content
description: Generated when an activity starts.
old-location: cos\icomactivityevents_onactivitycreate.htm
old-project: cossdk
ms.assetid: 27d6dfd6-24c8-480b-9d91-6c6cce08384c
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityCreate method, IComActivityEvents.OnActivityCreate, IComActivityEvents::OnActivityCreate, OnActivityCreate, OnActivityCreate method [COM+], OnActivityCreate method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityCreate, comsvcs/IComActivityEvents::OnActivityCreate, cos.icomactivityevents_onactivitycreate
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
 - IComActivityEvents.OnActivityCreate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComActivityEvents::OnActivityCreate


## -description


Generated when an activity starts.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The GUID associated with the current activity.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/9b702bcd-d5a6-41fa-98ce-00a245dfe770">IComActivityEvents</a>
 

 

