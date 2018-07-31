---
UID: NF:tapi.lineGetAgentGroupListA
title: lineGetAgentGroupListA function
author: windows-sdk-content
description: The lineGetAgentGroupList function obtains the identities of agent groups (combination of queue, supervisor, skill level, and so on) into which the agent currently logged in on the workstation is permitted to log into on the automatic call distributor.
old-location: tapi2\linegetagentgrouplist.htm
old-project: Tapi
ms.assetid: b3767efd-8f7a-4a03-81f6-97e11994900d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "_tapi2_linegetagentgrouplist, lineGetAgentGroupList, lineGetAgentGroupList function [TAPI 2.2], lineGetAgentGroupListA, lineGetAgentGroupListW, tapi/lineGetAgentGroupList, tapi/lineGetAgentGroupListA, tapi/lineGetAgentGroupListW, tapi2.linegetagentgrouplist"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAgentGroupListW (Unicode) and lineGetAgentGroupListA (ANSI)
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
 - lineGetAgentGroupList
 - lineGetAgentGroupListA
 - lineGetAgentGroupListW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetAgentGroupListA function


## -description


The 
<b>lineGetAgentGroupList</b> function obtains the identities of agent groups (combination of queue, supervisor, skill level, and so on) into which the agent currently logged in on the workstation is permitted to log into on the automatic call distributor.


## -parameters




### -param hLine

Handle to the open line device.


### -param dwAddressID

Address on the open line device whose agent status is to be queried.


### -param lpAgentGroupList

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>. Upon successful completion of the request, this structure is filled with a list of the agent groups into which the agent can log in at this time (which should include any groups into which the agent is already logged in, if any).


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, this function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALAGENTID, LINEERR_INVALLINEHANDLE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

