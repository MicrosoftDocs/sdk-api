---
UID: NF:tapi.lineCreateAgentSessionW
title: lineCreateAgentSessionW function (tapi.h)
description: The lineCreateAgentSession function creates a new AgentSession object. It generates a LINE_PROXYREQUEST message to be sent to a registered proxy function handler, referencing a LINEPROXYREQUEST structure of type LINEPROXYREQUEST_CREATEAGENTSESSION. (Unicode)
helpviewer_keywords: ["_tapi2_linecreateagentsession", "lineCreateAgentSession", "lineCreateAgentSession function [TAPI 2.2]", "lineCreateAgentSessionW", "tapi/lineCreateAgentSession", "tapi/lineCreateAgentSessionW", "tapi2.linecreateagentsession"]
old-location: tapi2\linecreateagentsession.htm
tech.root: tapi3
ms.assetid: 38b080d9-365f-49b6-a125-625602971bb8
ms.date: 12/05/2018
ms.keywords: _tapi2_linecreateagentsession, lineCreateAgentSession, lineCreateAgentSession function [TAPI 2.2], lineCreateAgentSessionA, lineCreateAgentSessionW, tapi/lineCreateAgentSession, tapi/lineCreateAgentSessionA, tapi/lineCreateAgentSessionW, tapi2.linecreateagentsession
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineCreateAgentSessionW
 - tapi/lineCreateAgentSessionW
dev_langs:
 - c++
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
---

# lineCreateAgentSessionW function


## -description

The 
<b>lineCreateAgentSession</b> function creates a new AgentSession object. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_CREATEAGENTSESSION.

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

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineCreateAgentSession as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
