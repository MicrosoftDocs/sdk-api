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

# IInvokeProvider::Invoke


## -description


Sends a request to activate a control and initiate its single, unambiguous action.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IInvokeProvider::Invoke</b> is an asynchronous call and must return immediately without blocking. 
        

<div class="alert"><b>Note</b>  
        This is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked. 
        Any Microsoft UI Automation client that instigated the event will remain blocked until the modal dialog is closed.
        </div>
<div> </div>
<b>IInvokeProvider::Invoke</b> raises the Invoked event after the control 
			has completed its associated action, if possible. 
            


            The event should be raised before servicing the Invoke request 
			in the following scenarios:
	

<ul>
<li>It is not possible or practical to wait until the action is complete.</li>
<li>The action requires user interaction.</li>
<li>The action is time-consuming and will cause the calling client to block for a significant length of time.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e522b8d5-c6f6-4f71-a8c8-4332f2824f72">IInvokeProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

