---
UID: NF:tapi.lineGetAgentGroupListA
title: lineGetAgentGroupListA function (tapi.h)
description: The lineGetAgentGroupList function obtains the identities of agent groups (combination of queue, supervisor, skill level, and so on) into which the agent currently logged in on the workstation is permitted to log into on the automatic call distributor. (ANSI)
helpviewer_keywords: ["lineGetAgentGroupListA", "tapi/lineGetAgentGroupListA"]
old-location: tapi2\linegetagentgrouplist.htm
tech.root: tapi3
ms.assetid: b3767efd-8f7a-4a03-81f6-97e11994900d
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetagentgrouplist, lineGetAgentGroupList, lineGetAgentGroupList function [TAPI 2.2], lineGetAgentGroupListA, lineGetAgentGroupListW, tapi/lineGetAgentGroupList, tapi/lineGetAgentGroupListA, tapi/lineGetAgentGroupListW, tapi2.linegetagentgrouplist
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAgentGroupListW (Unicode) and lineGetAgentGroupListA (ANSI)
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
 - lineGetAgentGroupListA
 - tapi/lineGetAgentGroupListA
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
 - lineGetAgentGroupList
 - lineGetAgentGroupListA
 - lineGetAgentGroupListW
---

# lineGetAgentGroupListA function


## -description

The 
<b>lineGetAgentGroupList</b> function obtains the identities of agent groups (combination of queue, supervisor, skill level, and so on) into which the agent currently logged in on the workstation is permitted to log into on the automatic call distributor.

## -parameters

### -param hLine

Handle to the open line device.

### -param dwAddressID

Address on the open line device whose agent status is to be queried.

### -param lpAgentGroupList

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a>. Upon successful completion of the request, this structure is filled with a list of the agent groups into which the agent can log in at this time (which should include any groups into which the agent is already logged in, if any).

## -returns

Returns a positive request identifier if the asynchronous operation starts; otherwise, this function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALAGENTID, LINEERR_INVALLINEHANDLE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineGetAgentGroupList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
