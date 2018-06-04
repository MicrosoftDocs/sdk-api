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

# TCI_MOD_FLOW_COMPLETE_HANDLER callback function


## -description


The 
<b>ClModifyFlowComplete</b> function is used by traffic control to notify the client of the completion of its previous call to the 
<a href="https://msdn.microsoft.com/e1b5d987-8365-4fea-a88b-0d574749b38a">TcModifyFlow</a> function.

The 
<b>ClModifyFlowComplete</b> callback function is optional. If this function is not specified, 
<a href="https://msdn.microsoft.com/e1b5d987-8365-4fea-a88b-0d574749b38a">TcModifyFlow</a> will block until it completes.


## -parameters




### -param ClFlowCtx [in]

Client provided–flow context handle. This can be the container used to hold an arbitrary client-defined context for this instance of the client. This value will be the same as the value provided by the client during its corresponding call to 
<a href="https://msdn.microsoft.com/e1b5d987-8365-4fea-a88b-0d574749b38a">TcModifyFlow</a>.


### -param Status [in]

Completion status for the 
<a href="https://msdn.microsoft.com/e1b5d987-8365-4fea-a88b-0d574749b38a">TcModifyFlow</a> request. This value may be any of the return values possible for the 
<b>TcModifyFlow</b> function, with the exception of ERROR_SIGNAL_PENDING. 




<div class="alert"><b>Note</b>  Use of the 
<b>ClModifyFlowComplete</b> function requires administrative privilege.</div>
<div> </div>

## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e1b5d987-8365-4fea-a88b-0d574749b38a">TcModifyFlow</a>
 

 

