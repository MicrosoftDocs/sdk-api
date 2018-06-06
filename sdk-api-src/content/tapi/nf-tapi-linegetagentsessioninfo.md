---
UID: NF:tapi.lineGetAgentSessionInfo
title: lineGetAgentSessionInfo function
author: windows-sdk-content
description: The lineGetAgentSessionInfo function returns a structure that holds the ACD information associated with a particular agent session handle.
old-location: tapi2\linegetagentsessioninfo.htm
old-project: Tapi
ms.assetid: 06a5ea23-4205-46fd-abe7-ee4575be81c8
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_linegetagentsessioninfo, lineGetAgentSessionInfo, lineGetAgentSessionInfo function [TAPI 2.2], tapi/lineGetAgentSessionInfo, tapi2.linegetagentsessioninfo"
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
req.unicode-ansi: 
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
 - lineGetAgentSessionInfo
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetAgentSessionInfo function


## -description


The 
<b>lineGetAgentSessionInfo</b> function returns a structure that holds the ACD information associated with a particular agent session handle. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETAGENTSESSIONINFO.


## -parameters




### -param hLine

Handle to the line device.


### -param hAgentSession

Identifier of the agent session whose information is to be retrieved.


### -param lpAgentSessionInfo

Pointer to a structure of type 
<a href="https://msdn.microsoft.com/567e21b4-c79c-4a54-b9f4-6c8c949bf4ee">LINEAGENTSESSIONINFO</a>. Upon successful completion of the request, this structure is filled with the agent session statistics. Prior to calling the 
<b>lineGetAgentSessionInfo</b> function, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that memory could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/567e21b4-c79c-4a54-b9f4-6c8c949bf4ee">LINEAGENTSESSIONINFO</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

