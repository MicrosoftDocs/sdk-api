---
UID: NF:tapi.lineGetAgentActivityListW
title: lineGetAgentActivityListW function (tapi.h)
description: The lineGetAgentActivityList function obtains the identities of activities that the application can select using lineSetAgentActivity to indicate what function the agent is actually performing at the moment. (Unicode)
helpviewer_keywords: ["_tapi2_linegetagentactivitylist", "lineGetAgentActivityList", "lineGetAgentActivityList function [TAPI 2.2]", "lineGetAgentActivityListW", "tapi/lineGetAgentActivityList", "tapi/lineGetAgentActivityListW", "tapi2.linegetagentactivitylist"]
old-location: tapi2\linegetagentactivitylist.htm
tech.root: tapi3
ms.assetid: 8f0be375-2891-45bd-a2cb-246ea5c4b9bb
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetagentactivitylist, lineGetAgentActivityList, lineGetAgentActivityList function [TAPI 2.2], lineGetAgentActivityListA, lineGetAgentActivityListW, tapi/lineGetAgentActivityList, tapi/lineGetAgentActivityListA, tapi/lineGetAgentActivityListW, tapi2.linegetagentactivitylist
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAgentActivityListW (Unicode) and lineGetAgentActivityListA (ANSI)
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
 - lineGetAgentActivityListW
 - tapi/lineGetAgentActivityListW
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
 - lineGetAgentActivityList
 - lineGetAgentActivityListA
 - lineGetAgentActivityListW
---

# lineGetAgentActivityListW function


## -description

The 
<b>lineGetAgentActivityList</b> function obtains the identities of activities that the application can select using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentactivity">lineSetAgentActivity</a> to indicate what function the agent is actually performing at the moment.

## -parameters

### -param hLine

Handle to the open line device.

### -param dwAddressID

Address on the open line device whose agent status is to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param lpAgentActivityList

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentactivitylist">LINEAGENTACTIVITYLIST</a>. Upon successful completion of the request, this structure is filled with a list of the agent activity codes that can be selected using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentactivity">lineSetAgentActivity</a>. Prior to calling 
<b>lineGetAgentActivityList</b>, the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns a positive request identifier if the asynchronous operation starts; otherwise, this function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALAGENTID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineagentactivitylist">LINEAGENTACTIVITYLIST</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentactivity">lineSetAgentActivity</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineGetAgentActivityList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
