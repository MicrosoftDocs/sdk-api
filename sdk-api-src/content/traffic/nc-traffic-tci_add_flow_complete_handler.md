---
UID: NC:traffic.TCI_ADD_FLOW_COMPLETE_HANDLER
title: TCI_ADD_FLOW_COMPLETE_HANDLER
author: windows-sdk-content
description: The ClAddFlowComplete function is used by traffic control to notify the client of the completion of its previous call to the TcAddFlow function.
old-location: qos\claddflowcomplete.htm
old-project: qos
ms.assetid: 0aa6f590-f7b2-4312-87a7-3854f883fa22
ms.author: windowssdkdev
ms.date: 03/26/2018
ms.keywords: ClAddFlowComplete, ClAddFlowComplete callback, ClAddFlowComplete callback function [QOS], TCI_ADD_FLOW_COMPLETE_HANDLER, TCI_ADD_FLOW_COMPLETE_HANDLER callback function [QOS], _gqos_claddflowcomplete, qos.claddflowcomplete, traffic/ClAddFlowComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: traffic.h
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
req.typenames: TPMVSCMGR_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Traffic.h
api_name:
 - TCI_ADD_FLOW_COMPLETE_HANDLER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TCI_ADD_FLOW_COMPLETE_HANDLER callback function


## -description


The 
<b>ClAddFlowComplete</b> function is used by traffic control to notify the client of the completion of its previous call to the 
<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a> function.

The 
<b>ClAddFlowComplete</b> callback function is optional. If this function is not specified, 
<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a> will block until it completes.


## -parameters




### -param ClFlowCtx [in]

Client provided–flow context handle. This can be the container used to hold an arbitrary client-defined context for this instance of the client. This value will be the same as the value provided by the client during its corresponding call to 
<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a>.


### -param Status [in]

Completion status for the 
<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a> request. This value may be any of the return values possible for the 
<b>TcAddFlow</b> function, with the exception of ERROR_SIGNAL_PENDING. 




<div class="alert"><b>Note</b>  Use of the 
<b>ClAddFlowComplete</b> function requires administrative privilege.</div>
<div> </div>

## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a>
 

 

