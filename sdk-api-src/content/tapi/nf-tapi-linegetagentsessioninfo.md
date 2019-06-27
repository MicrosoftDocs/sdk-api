---
UID: NF:tapi.lineGetAgentSessionInfo
title: lineGetAgentSessionInfo function (tapi.h)
author: windows-sdk-content
description: The lineGetAgentSessionInfo function returns a structure that holds the ACD information associated with a particular agent session handle.
old-location: tapi2\linegetagentsessioninfo.htm
tech.root: Tapi
ms.assetid: 06a5ea23-4205-46fd-abe7-ee4575be81c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linegetagentsessioninfo, lineGetAgentSessionInfo, lineGetAgentSessionInfo function [TAPI 2.2], tapi/lineGetAgentSessionInfo, tapi2.linegetagentsessioninfo"
ms.topic: function
f1_keywords: 
 - "tapi/lineGetAgentSessionInfo"
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
 - lineGetAgentSessionInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineGetAgentSessionInfo function


## -description


The 
<b>lineGetAgentSessionInfo</b> function returns a structure that holds the ACD information associated with a particular agent session handle. It generates a 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest_tag">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETAGENTSESSIONINFO.


## -parameters




### -param hLine

Handle to the line device.


### -param hAgentSession

Identifier of the agent session whose information is to be retrieved.


### -param lpAgentSessionInfo

Pointer to a structure of type 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentsessioninfo_tag">LINEAGENTSESSIONINFO</a>. Upon successful completion of the request, this structure is filled with the agent session statistics. Prior to calling the 
<b>lineGetAgentSessionInfo</b> function, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that memory could get overwritten. For more information on setting structure sizes, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentsessioninfo_tag">LINEAGENTSESSIONINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest_tag">LINEPROXYREQUEST</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>
 

 

