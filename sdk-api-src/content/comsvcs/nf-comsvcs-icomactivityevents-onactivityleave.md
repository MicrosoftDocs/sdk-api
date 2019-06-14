---
UID: NF:comsvcs.IComActivityEvents.OnActivityLeave
title: IComActivityEvents::OnActivityLeave (comsvcs.h)
author: windows-sdk-content
description: Generated when an activity thread is left.
old-location: cos\icomactivityevents_onactivityleave.htm
tech.root: cossdk
ms.assetid: f39a8ce1-9c17-47eb-9405-c6a69dee88cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComActivityEvents interface [COM+],OnActivityLeave method, IComActivityEvents.OnActivityLeave, IComActivityEvents::OnActivityLeave, OnActivityLeave, OnActivityLeave method [COM+], OnActivityLeave method [COM+],IComActivityEvents interface, _dtc_IComActivityEvents_OnActivityLeave, comsvcs/IComActivityEvents::OnActivityLeave, cos.icomactivityevents_onactivityleave
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
ms.custom: 19H1
---

# IComActivityEvents::OnActivityLeave


## -description


Generated when an activity thread is left.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param guidCurrent [in]

The GUID associated with the caller.


### -param guidLeft [in]

The GUID associated with the activity thread left.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomactivityevents">IComActivityEvents</a>
 

 

