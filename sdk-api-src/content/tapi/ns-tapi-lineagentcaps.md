---
UID: NS:tapi.lineagentcaps_tag
title: LINEAGENTCAPS (tapi.h)
description: The LINEAGENTCAPS structure describes the capabilities of an ACD agent. The lineGetAgentCaps function returns the LINEAGENTCAPS structure.
helpviewer_keywords: ["*LPLINEAGENTCAPS","LINEAGENTCAPS","LINEAGENTCAPS structure [TAPI 2.2]","LPLINEAGENTCAPS","LPLINEAGENTCAPS structure pointer [TAPI 2.2]","_tapi2_lineagentcaps_str","tapi/LINEAGENTCAPS","tapi/LPLINEAGENTCAPS","tapi2.lineagentcaps_str"]
old-location: tapi2\lineagentcaps_str.htm
tech.root: tapi3
ms.assetid: e4c5ece8-7b29-4154-9b38-f2b17049446f
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTCAPS, LINEAGENTCAPS, LINEAGENTCAPS structure [TAPI 2.2], LPLINEAGENTCAPS, LPLINEAGENTCAPS structure pointer [TAPI 2.2], _tapi2_lineagentcaps_str, tapi/LINEAGENTCAPS, tapi/LPLINEAGENTCAPS, tapi2.lineagentcaps_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINEAGENTCAPS, *LPLINEAGENTCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentcaps_tag
 - tapi/lineagentcaps_tag
 - LPLINEAGENTCAPS
 - tapi/LPLINEAGENTCAPS
 - LINEAGENTCAPS
 - tapi/LINEAGENTCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAGENTCAPS
---

# LINEAGENTCAPS structure


## -description

The 
<b>LINEAGENTCAPS</b> structure describes the capabilities of an ACD agent. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentcapsa">lineGetAgentCaps</a> function returns the 
<b>LINEAGENTCAPS</b> structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwAgentHandlerInfoSize

Size of the agent handler information, in bytes.

### -field dwAgentHandlerInfoOffset

Offset from the beginning of the structure to a null-terminated string specifying the name, version, or other identifying information of the server application that is handling agent requests. The size of the string is specified by <b>dwAgentHandlerInfoSize</b>.

### -field dwCapsVersion

TAPI version that the agent handler application used in preparing the contents of this structure. This is no greater than the API version that the calling application passed in to 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentcapsa">lineGetAgentCaps</a>.

### -field dwFeatures

Agent-related features available for this line using the 
<a href="/windows/desktop/Tapi/lineagentfeature--constants">LINEAGENTFEATURE_ constants</a>. Invoking a supported feature requires the line and address to be in the proper state. A zero in a bit position indicates that the corresponding feature is never available. A one indicates that the corresponding feature may be available if the line is in the appropriate state for the operation to be meaningful. This field allows an application to discover which agent features can be (and which can never be) supported by the device.

### -field dwStates

<a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ constants</a> that can be used in the <i>dwAgentState</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentState</a>. Setting a supported state requires the line and address to be in the proper state. A zero in a bit position indicates that the corresponding state is never available. A one indicates that the corresponding state may be available if the line is in the appropriate state for the state to be meaningful. This field allows an application to discover which agent states can be (and which can never be) supported on the device.

### -field dwNextStates

LINEAGENTSTATE_ constants that can be used in the <i>dwNextAgentState</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentState</a>. Setting a supported state requires the line and address to be in the proper state. A zero in a bit position indicates that the corresponding state is never available. A one indicates that the corresponding state may be available if the line is in the appropriate state for the state to be meaningful. This field allows an application to discover which agent states can be (and which can never be) supported on the device.

### -field dwMaxNumGroupEntries

Maximum number of agent identifiers that can be logged in on the address simultaneously. Determines the highest value that can be passed in as the <b>dwNumEntries</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a> structure to 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentgroup">lineSetAgentGroup</a>.

### -field dwAgentStatusMessages

Indicates the 
<a href="/windows/desktop/Tapi/lineagentstatus--constants">LINEAGENTSTATUS_ constants</a> that can be received by the application in <i>dwParam2</i> of a 
<a href="/windows/desktop/Tapi/line-agentstatus">LINE_AGENTSTATUS</a> message.

### -field dwNumAgentExtensionIDs

Number of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a> structures that appear in the <i>ExtensionIDList</i> array. The value is 0 if agent-handler-specific extensions are supported on the address.

### -field dwAgentExtensionIDListSize

Size of the agent extension IDs array, in bytes.

### -field dwAgentExtensionIDListOffset

Offset from the beginning of the structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a> structures. The size is <b>dwNumExtensionIDs</b> times SIZEOF(LINEEXTENSIONID). The array lists the 128-bit universally unique identifiers for all agent-handler-specific extensions supported by the agent handle for the address. The extension being used is referenced in the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineagentspecific">lineAgentSpecific</a> function and 
<a href="/windows/desktop/Tapi/line-agentspecific">LINE_AGENTSPECIFIC</a> message by its position in this table, the first entry being entry 0, so it is important that the agent handler always present extension identifiers in this array in the same order. The size of the array is specified by <b>dwAgentExtensionIDListOffset</b>.

### -field ProxyGUID

GUID for ACD proxy associated with the line. This element is exposed only to applications that negotiate a TAPI version of 2.2 or higher.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-agentspecific">LINE_AGENTSPECIFIC</a>



<a href="/windows/desktop/Tapi/line-agentstatus">LINE_AGENTSTATUS</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineagentspecific">lineAgentSpecific</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentcapsa">lineGetAgentCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentgroup">lineSetAgentGroup</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentState</a>