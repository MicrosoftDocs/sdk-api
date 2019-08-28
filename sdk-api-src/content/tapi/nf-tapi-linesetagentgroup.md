---
UID: NF:tapi.lineSetAgentGroup
title: lineSetAgentGroup function (tapi.h)
author: windows-sdk-content
description: The lineSetAgentGroup function sets the agent groups into which the agent is logged into on a particular address.
old-location: tapi2\linesetagentgroup.htm
tech.root: Tapi
ms.assetid: ce6795fb-fe11-4125-abeb-9b2686ea669a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linesetagentgroup, lineSetAgentGroup, lineSetAgentGroup function [TAPI 2.2], tapi/lineSetAgentGroup, tapi2.linesetagentgroup"
ms.topic: function
f1_keywords: 
 - "tapi/lineSetAgentGroup"
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
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a> structure identifying the groups into which the current agent is to be logged in on the address. If the pointer is <b>NULL</b> or the number of groups in the indicated structure is zero, then the agent is logged out of any ACD groups into which it is currently logged in. 

The "Name" fields in the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a> items in the list are ignored for purposes of this function; the control of the logged-in groups is based on the group identifier values only.


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALADDRESSSTATE, LINEERR_INVALAGENTGROUP, LINEERR_INVALAGENTID, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_INVALPASSWORD, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
 

 

