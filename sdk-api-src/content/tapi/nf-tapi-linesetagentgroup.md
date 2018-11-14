---
UID: NF:tapi.lineSetAgentGroup
title: lineSetAgentGroup function
author: windows-sdk-content
description: The lineSetAgentGroup function sets the agent groups into which the agent is logged into on a particular address.
old-location: tapi2\linesetagentgroup.htm
tech.root: tapi
ms.assetid: ce6795fb-fe11-4125-abeb-9b2686ea669a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_tapi2_linesetagentgroup, lineSetAgentGroup, lineSetAgentGroup function [TAPI 2.2], tapi/lineSetAgentGroup, tapi2.linesetagentgroup"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
 - lineSetAgentGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- lineSetAgentGroup
: 
---

# lineSetAgentGroup function


## -description


The 
<b>lineSetAgentGroup</b> function sets the agent groups into which the agent is logged into on a particular address.


## -parameters




### -param hLine

Handle to the line device.


### -param dwAddressID

Identifier of the address for which the agent information is to be changed. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param lpAgentGroupList

Pointer to a 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a> structure identifying the groups into which the current agent is to be logged in on the address. If the pointer is <b>NULL</b> or the number of groups in the indicated structure is zero, then the agent is logged out of any ACD groups into which it is currently logged in. 

The "Name" fields in the 
<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a> items in the list are ignored for purposes of this function; the control of the logged-in groups is based on the group identifier values only.


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALADDRESSSTATE, LINEERR_INVALAGENTGROUP, LINEERR_INVALAGENTID, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_INVALPASSWORD, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a>



<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

