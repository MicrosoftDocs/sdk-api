---
UID: NC:traffic.TCI_DEL_FLOW_COMPLETE_HANDLER
title: TCI_DEL_FLOW_COMPLETE_HANDLER (traffic.h)
description: The ClDeleteFlowComplete function is used by traffic control to notify the client of the completion of its previous call to the TcDeleteFlow function.
helpviewer_keywords: ["ClDeleteFlowComplete","ClDeleteFlowComplete callback","ClDeleteFlowComplete callback function [QOS]","TCI_DEL_FLOW_COMPLETE_HANDLER","TCI_DEL_FLOW_COMPLETE_HANDLER callback function [QOS]","_gqos_cldeleteflowcomplete","qos.cldeleteflowcomplete","traffic/ClDeleteFlowComplete"]
old-location: qos\cldeleteflowcomplete.htm
tech.root: QOS
ms.assetid: b31bd6e5-2b72-407d-a77e-ff9cee8de238
ms.date: 12/05/2018
ms.keywords: ClDeleteFlowComplete, ClDeleteFlowComplete callback, ClDeleteFlowComplete callback function [QOS], TCI_DEL_FLOW_COMPLETE_HANDLER, TCI_DEL_FLOW_COMPLETE_HANDLER callback function [QOS], _gqos_cldeleteflowcomplete, qos.cldeleteflowcomplete, traffic/ClDeleteFlowComplete
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TCI_DEL_FLOW_COMPLETE_HANDLER
 - traffic/TCI_DEL_FLOW_COMPLETE_HANDLER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Traffic.h
api_name:
 - TCI_DEL_FLOW_COMPLETE_HANDLER
---

# TCI_DEL_FLOW_COMPLETE_HANDLER callback function


## -description

The 
<b>ClDeleteFlowComplete</b> function is used by traffic control to notify the client of the completion of its previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a> function.

The 
<b>ClDeleteFlowComplete</b> callback function is optional. If this function is not specified, 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a> will block until it completes.

## -parameters

### -param ClFlowCtx [in]

Client provided–flow context handle. This can be the container used to hold an arbitrary client-defined context for this instance of the client. This value will be the same as the value provided by the client during its corresponding call to 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a>.

### -param Status [in]

Completion status for the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a> request. This value may be any of the return values possible for the 
<b>TcDeleteFlow</b> function, with the exception of ERROR_SIGNAL_PENDING. 




<div class="alert"><b>Note</b>  Use of the 
<b>ClDeleteFlowComplete</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a>