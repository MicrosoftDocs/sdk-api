---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWbemServices::QueryObjectSink


## -description


The <b>IWbemServices::QueryObjectSink</b> method 
  allows the caller to obtain a notification handler that is exported by Windows Management. This allows the caller 
  to write notifications and events directly to Windows Management. The caller should only write extrinsic events to 
  Windows Management. For more information, see 
  <a href="https://msdn.microsoft.com/46cdfcfa-42c6-4169-bc4d-725867224889">Determining the Type of Event to Receive</a>.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param ppResponseHandler [out]

Receives the interface pointer to the notification handler. This is set to point to <b>NULL</b> when there is an error. The returned pointer has a positive reference count, and the caller must call <b>IWbemServices::Release</b> on the pointer when it is no longer needed. A <b>NULL</b> value can be returned if no notification handler is available. This is not an error.

<div class="alert"><b>Note</b>  The value of the <i>ppResponseHandler</i> parameter cannot be <b>NULL</b> when it is passed to this method.</div>
<div> </div>

## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

<div class="alert"><b>Note</b>  Firing events using <b>QueryObjectSink</b> 
    is permitted by default for Administrators only. Extending the permission to other users requires giving them 
  <b>WBEM_FULL_WRITE</b> permission.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/0cceda42-fba0-4a08-90dd-43f022d0be41">Querying WMI</a>
 

 

