---
UID: NF:tapi.lineSetAgentActivity
title: lineSetAgentActivity function (tapi.h)
description: The lineSetAgentActivity function sets the agent activity code associated with a particular address.
helpviewer_keywords: ["_tapi2_linesetagentactivity","lineSetAgentActivity","lineSetAgentActivity function [TAPI 2.2]","tapi/lineSetAgentActivity","tapi2.linesetagentactivity"]
old-location: tapi2\linesetagentactivity.htm
tech.root: tapi3
ms.assetid: 2c46e1cb-e2d7-4cb5-b937-55011058fd15
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetagentactivity, lineSetAgentActivity, lineSetAgentActivity function [TAPI 2.2], tapi/lineSetAgentActivity, tapi2.linesetagentactivity
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSetAgentActivity
 - tapi/lineSetAgentActivity
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
 - lineSetAgentActivity
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

<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>