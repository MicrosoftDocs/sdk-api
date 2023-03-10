---
UID: NF:tapi.lineAgentSpecific
title: lineAgentSpecific function (tapi.h)
description: The lineAgentSpecific function allows the application to access proprietary handler-specific functions of the agent handler associated with the address.
helpviewer_keywords: ["_tapi2_lineagentspecific","lineAgentSpecific","lineAgentSpecific function [TAPI 2.2]","tapi/lineAgentSpecific","tapi2.lineagentspecific"]
old-location: tapi2\lineagentspecific.htm
tech.root: tapi3
ms.assetid: 4a1f2be4-4465-418a-9717-3857acf930a4
ms.date: 12/05/2018
ms.keywords: _tapi2_lineagentspecific, lineAgentSpecific, lineAgentSpecific function [TAPI 2.2], tapi/lineAgentSpecific, tapi2.lineagentspecific
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
 - lineAgentSpecific
 - tapi/lineAgentSpecific
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
 - lineAgentSpecific
---

# lineAgentSpecific function


## -description

The 
<b>lineAgentSpecific</b> function allows the application to access proprietary handler-specific functions of the agent handler associated with the address. The meaning of the extensions are specific to the agent handler. Each set of agent-related extensions is identified by a universally unique 128-bit extension ID that must be obtained, along with the specification for the extension, from the promulgator of that extension (usually the author of the agent handler software on the telephony server). The list of extensions supported by the agent handler is obtained from the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentcaps">LINEAGENTCAPS</a> structure returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentcapsa">lineGetAgentCaps</a>.

## -parameters

### -param hLine

Handle to the open line device.

### -param dwAddressID

Address on the open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param dwAgentExtensionIDIndex

Position in the <b>ExtensionIDList</b> structure in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentcaps">LINEAGENTCAPS</a> of the agent handler extension being invoked.

### -param lpParams

Pointer to a memory area used to hold a parameter block. The format of this parameter block is device specific and its contents are passed by TAPI to and from the agent handler application on the telephony server. This parameter block must specify the function to be invoked and include sufficient room for any data to be returned.

### -param dwSize

Size of the parameter block area, in bytes. 




<div class="alert"><b>Note</b>  If <i>lpParams</i> is a pointer to a string, the size must include the <b>NULL</b> terminator. </div>
<div> </div>

## -returns

Returns a positive request identifier if the asynchronous operation starts; otherwise, this function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALAGENTID, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_UNINITIALIZED.

Additional return values are specific to the agent handler.

## -remarks

This operation is part of the Extended Telephony services. It provides access to an agent handler-specific feature without defining its meaning.

This function provides a generic parameter profile. The interpretation of the parameter structure is handler specific. Indications and replies sent back to the application that are handler specific should use the 
<a href="/windows/desktop/Tapi/line-agentspecific">LINE_AGENTSPECIFIC</a> message.

An agent handler can provide access to handler-specific functions by defining parameters for use with this function. Applications that want to make use of these extensions should consult the vendor-specific documentation that describes what extensions are defined. Typically, an application that relies on these extensions is not able to work with other agent handler environments.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineagentcaps">LINEAGENTCAPS</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentcapsa">lineGetAgentCaps</a>