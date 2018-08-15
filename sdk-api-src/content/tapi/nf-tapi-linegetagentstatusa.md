---
UID: NF:tapi.lineGetAgentStatusA
title: lineGetAgentStatusA function
author: windows-sdk-content
description: The lineGetAgentStatus function obtains the agent-related status on the specified address.
old-location: tapi2\linegetagentstatus.htm
old-project: tapi
ms.assetid: 6736cde5-af38-493d-b09a-a807d9e9a382
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linegetagentstatus, lineGetAgentStatus, lineGetAgentStatus function [TAPI 2.2], lineGetAgentStatusA, lineGetAgentStatusW, tapi/lineGetAgentStatus, tapi/lineGetAgentStatusA, tapi/lineGetAgentStatusW, tapi2.linegetagentstatus"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAgentStatusW (Unicode) and lineGetAgentStatusA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetAgentStatus
 - lineGetAgentStatusA
 - lineGetAgentStatusW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetAgentStatusA function


## -description


The 
<b>lineGetAgentStatus</b> function obtains the agent-related status on the specified address.


## -parameters




### -param hLine

Handle to the open line device.


### -param dwAddressID

Address on the open line device whose agent status is to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param lpAgentStatus

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/c846bd16-79d2-4af0-b3ad-7432c28c542b">LINEAGENTSTATUS</a>. Upon successful completion of the request, this structure is filled with agent status information. Prior to calling 
<b>lineGetAgentStatus</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that memory could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALLINEHANDLE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/c846bd16-79d2-4af0-b3ad-7432c28c542b">LINEAGENTSTATUS</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

