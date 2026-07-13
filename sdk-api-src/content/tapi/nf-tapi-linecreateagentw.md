---
UID: NF:tapi.lineCreateAgentW
title: lineCreateAgentW function (tapi.h)
description: The lineCreateAgent function creates a new Agent object. It generates a LINE_PROXYREQUEST message to be sent to a registered proxy function handler, referencing a LINEPROXYREQUEST structure of type LINEPROXYREQUEST_CREATEAGENT. (Unicode)
helpviewer_keywords: ["_tapi2_linecreateagent", "lineCreateAgent", "lineCreateAgent function [TAPI 2.2]", "lineCreateAgentW", "tapi/lineCreateAgent", "tapi/lineCreateAgentW", "tapi2.linecreateagent"]
old-location: tapi2\linecreateagent.htm
tech.root: tapi3
ms.assetid: 14b2e9c8-32ab-42c0-acfa-17a0f8a9b73f
ms.date: 12/05/2018
ms.keywords: _tapi2_linecreateagent, lineCreateAgent, lineCreateAgent function [TAPI 2.2], lineCreateAgentA, lineCreateAgentW, tapi/lineCreateAgent, tapi/lineCreateAgentA, tapi/lineCreateAgentW, tapi2.linecreateagent
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineCreateAgentW (Unicode) and lineCreateAgentA (ANSI)
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
 - lineCreateAgentW
 - tapi/lineCreateAgentW
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
 - lineCreateAgent
 - lineCreateAgentA
 - lineCreateAgentW
---

# lineCreateAgentW function


## -description

The 
<b>lineCreateAgent</b> function creates a new Agent object. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_CREATEAGENT.

## -parameters

### -param hLine

Handle to the line device.

### -param lpszAgentID

Pointer to a <b>null</b>-terminated Unicode string containing the agent identifier. Used when working with legacy ACD systems. With an ACD system that uses the operating system's user login for authentication, <i>lpszAgentID</i> is set to <b>NULL</b>.

### -param lpszAgentPIN

Pointer to a <b>null</b>-terminated Unicode string containing the agent PIN or password. Used when working with legacy ACD systems. With an ACD system that uses the operating system's user login for authentication, <i>lpszAgentPIN</i> is set to <b>NULL</b>.

### -param lphAgent

Handle to the created agent, returned by the ACD proxy. It is the responsibility of the agent handler proxy application to generate and maintain uniqueness of this identifier.

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineCreateAgent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
