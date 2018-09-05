---
UID: NC:traffic.TCI_MOD_FLOW_COMPLETE_HANDLER
title: TCI_MOD_FLOW_COMPLETE_HANDLER
author: windows-sdk-content
description: The ClModifyFlowComplete function is used by traffic control to notify the client of the completion of its previous call to the TcModifyFlow function.
old-location: qos\clmodifyflowcomplete.htm
old-project: QOS
ms.assetid: 61afc465-d942-4db7-96ee-56f3f1c3cafa
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClModifyFlowComplete, ClModifyFlowComplete callback, ClModifyFlowComplete callback function [QOS], TCI_MOD_FLOW_COMPLETE_HANDLER, TCI_MOD_FLOW_COMPLETE_HANDLER callback function [QOS], _gqos_clmodifyflowcomplete, qos.clmodifyflowcomplete, traffic/ClModifyFlowComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: traffic.h
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
req.typenames: TPMVSCMGR_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Traffic.h
api_name:
 - TCI_MOD_FLOW_COMPLETE_HANDLER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

