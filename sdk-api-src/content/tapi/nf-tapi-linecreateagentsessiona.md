---
UID: NF:tapi.lineCreateAgentSessionA
title: lineCreateAgentSessionA function
author: windows-sdk-content
description: The lineCreateAgentSession function creates a new AgentSession object. It generates a LINE_PROXYREQUEST message to be sent to a registered proxy function handler, referencing a LINEPROXYREQUEST structure of type LINEPROXYREQUEST_CREATEAGENTSESSION.
old-location: tapi2\linecreateagentsession.htm
tech.root: tapi
ms.assetid: 38b080d9-365f-49b6-a125-625602971bb8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linecreateagentsession, lineCreateAgentSession, lineCreateAgentSession function [TAPI 2.2], lineCreateAgentSessionA, lineCreateAgentSessionW, tapi/lineCreateAgentSession, tapi/lineCreateAgentSessionA, tapi/lineCreateAgentSessionW, tapi2.linecreateagentsession"
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
req.unicode-ansi: lineCreateAgentSessionW (Unicode) and lineCreateAgentSessionA (ANSI)
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
 - lineCreateAgentSession
 - lineCreateAgentSessionA
 - lineCreateAgentSessionW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineCreateAgentSessionA function


## -description


The 
<b>lineCreateAgentSession</b> function creates a new AgentSession object. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_CREATEAGENTSESSION.


## -parameters




### -param hLine

Handle to the line device.


### -param hAgent

Identifier of the agent for whom the session is to be created.


### -param lpszAgentPIN

Pointer to a <b>null</b>-terminated Unicode string containing the agent PIN or password. Used when working with legacy ACD systems that require a separate PIN for each session created (or group logged into). With an ACD system that uses the operating system's user login for authentication, <i>lpszAgentPIN</i> is set to <b>NULL</b>.


### -param dwWorkingAddressID

Identifier of the address on which the agent will receive calls for this session.


### -param lpGroupID

Pointer to a GUID that identifies the group for which the session is being created.


### -param lphAgentSession

Handle to the created agent session, returned by the ACD proxy. It is the responsibility of the agent handler proxy application to generate and maintain uniqueness of these identifiers.


## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

