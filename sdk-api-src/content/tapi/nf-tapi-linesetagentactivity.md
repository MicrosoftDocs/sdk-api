---
UID: NF:tapi.lineSetAgentActivity
title: lineSetAgentActivity function
author: windows-sdk-content
description: The lineSetAgentActivity function sets the agent activity code associated with a particular address.
old-location: tapi2\linesetagentactivity.htm
tech.root: Tapi
ms.assetid: 2c46e1cb-e2d7-4cb5-b937-55011058fd15
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_tapi2_linesetagentactivity, lineSetAgentActivity, lineSetAgentActivity function [TAPI 2.2], tapi/lineSetAgentActivity, tapi2.linesetagentactivity"
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
 - lineSetAgentActivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- lineSetAgentActivity
: 
---

# lineSetAgentActivity function


## -description


The 
<b>lineSetAgentActivity</b> function sets the agent activity code associated with a particular address.


## -parameters




### -param hLine

Handle to the line device.


### -param dwAddressID

Identifier of the address for which the agent activity code is to be changed. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param dwActivityID

New agent activity. The meaning of all values of this parameter are specific to the application and call center server.


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALADDRESSSTATE, LINEERR_INVALAGENTACTIVITY, LINEERR_INVALLINEHANDLE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

