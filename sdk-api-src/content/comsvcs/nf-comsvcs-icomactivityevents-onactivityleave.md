---
UID: NF:comsvcs.IComActivityEvents.OnActivityLeave
title: IComActivityEvents::OnActivityLeave
author: windows-sdk-content
description: Generated when an activity thread is left.
old-location: cos\icomactivityevents_onactivityleave.htm
tech.root: cossdk
ms.assetid: f39a8ce1-9c17-47eb-9405-c6a69dee88cc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityLeave method, IComActivityEvents.OnActivityLeave, IComActivityEvents::OnActivityLeave, OnActivityLeave, OnActivityLeave method [COM+], OnActivityLeave method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityLeave, comsvcs/IComActivityEvents::OnActivityLeave, cos.icomactivityevents_onactivityleave
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComActivityEvents.OnActivityLeave
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IComActivityEvents.OnActivityLeave
: 
---

# IComActivityEvents::OnActivityLeave


## -description


Generated when an activity thread is left.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidCurrent [in]

The GUID associated with the caller.


### -param guidLeft [in]

The GUID associated with the activity thread left.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684373(v=VS.85).aspx">IComActivityEvents</a>
 

 

