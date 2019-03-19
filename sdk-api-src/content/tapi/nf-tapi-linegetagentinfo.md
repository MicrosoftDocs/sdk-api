---
UID: NF:tapi.lineGetAgentInfo
title: lineGetAgentInfo function (tapi.h)
author: windows-sdk-content
description: The lineGetAgentInfo function returns a structure holding the ACD information associated with a particular agent handle.
old-location: tapi2\linegetagentinfo.htm
tech.root: Tapi
ms.assetid: 166b0595-2df0-431f-924c-6899b47408ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linegetagentinfo, lineGetAgentInfo, lineGetAgentInfo function [TAPI 2.2], tapi/lineGetAgentInfo, tapi2.linegetagentinfo"
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
 - lineGetAgentInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetAgentInfo function


## -description


The 
<b>lineGetAgentInfo</b> function returns a structure holding the ACD information associated with a particular agent handle. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETAGENTINFO.


## -parameters




### -param hLine

Handle to the line device.


### -param hAgent

Identifier of the agent whose information is to be retrieved.


### -param lpAgentInfo

Pointer to a structure of type 
<a href="https://msdn.microsoft.com/84eedf88-f0ea-4dc8-9840-b94a47fb7ca2">LINEAGENTINFO</a>. If the request succeeds, this structure is filled with the agent statistics. 


## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -remarks



Prior to calling the 
<b>lineGetAgentInfo</b> function, the application should set the <b>dwTotalSize</b> member of the 
<a href="https://msdn.microsoft.com/84eedf88-f0ea-4dc8-9840-b94a47fb7ca2">LINEAGENTINFO</a> structure to indicate the amount of memory available to TAPI for returning information.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/84eedf88-f0ea-4dc8-9840-b94a47fb7ca2">LINEAGENTINFO</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

