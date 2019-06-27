---
UID: NF:tapi.lineGetAgentStatusA
title: lineGetAgentStatusA function (tapi.h)
author: windows-sdk-content
description: The lineGetAgentStatus function obtains the agent-related status on the specified address.
old-location: tapi2\linegetagentstatus.htm
tech.root: Tapi
ms.assetid: 6736cde5-af38-493d-b09a-a807d9e9a382
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linegetagentstatus, lineGetAgentStatus, lineGetAgentStatus function [TAPI 2.2], lineGetAgentStatusA, lineGetAgentStatusW, tapi/lineGetAgentStatus, tapi/lineGetAgentStatusA, tapi/lineGetAgentStatusW, tapi2.linegetagentstatus"
ms.topic: function
f1_keywords: 
 - "tapi/lineGetAgentStatus"
req.header: tapi.h
req.include-header: 
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentstatus_tag">LINEAGENTSTATUS</a>. Upon successful completion of the request, this structure is filled with agent status information. Prior to calling 
<b>lineGetAgentStatus</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that memory could get overwritten. For more information on setting structure sizes, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALLINEHANDLE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentstatus_tag">LINEAGENTSTATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
 

 

