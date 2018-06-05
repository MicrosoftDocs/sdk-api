---
UID: NS:tapi.lineagentcaps_tag
title: lineagentcaps_tag
author: windows-sdk-content
description: The LINEAGENTCAPS structure describes the capabilities of an ACD agent. The lineGetAgentCaps function returns the LINEAGENTCAPS structure.
old-location: tapi2\lineagentcaps_str.htm
old-project: Tapi
ms.assetid: e4c5ece8-7b29-4154-9b38-f2b17049446f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPLINEAGENTCAPS, LINEAGENTCAPS, LINEAGENTCAPS structure [TAPI 2.2], LPLINEAGENTCAPS, LPLINEAGENTCAPS structure pointer [TAPI 2.2], _tapi2_lineagentcaps_str, lineagentcaps_tag, tapi/LINEAGENTCAPS, tapi/LPLINEAGENTCAPS, tapi2.lineagentcaps_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: LINEAGENTCAPS, *LPLINEAGENTCAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINEAGENTCAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineagentcaps_tag structure


## -description


The 
<b>LINEAGENTCAPS</b> structure describes the capabilities of an ACD agent. The 
<a href="https://msdn.microsoft.com/04bb6c00-2654-4707-ab11-2490ab5d9ab0">lineGetAgentCaps</a> function returns the 
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
<a href="https://msdn.microsoft.com/04bb6c00-2654-4707-ab11-2490ab5d9ab0">lineGetAgentCaps</a>.


### -field dwFeatures

Agent-related features available for this line using the 
<a href="https://msdn.microsoft.com/5953eb49-08ac-4c13-9fd3-df5473f96af8">LINEAGENTFEATURE_ constants</a>. Invoking a supported feature requires the line and address to be in the proper state. A zero in a bit position indicates that the corresponding feature is never available. A one indicates that the corresponding feature may be available if the line is in the appropriate state for the operation to be meaningful. This field allows an application to discover which agent features can be (and which can never be) supported by the device.


### -field dwStates


<a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ constants</a> that can be used in the <i>dwAgentState</i> parameter of 
<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentState</a>. Setting a supported state requires the line and address to be in the proper state. A zero in a bit position indicates that the corresponding state is never available. A one indicates that the corresponding state may be available if the line is in the appropriate state for the state to be meaningful. This field allows an application to discover which agent states can be (and which can never be) supported on the device.


### -field dwNextStates

LINEAGENTSTATE_ constants that can be used in the <i>dwNextAgentState</i> parameter of 
<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentState</a>. Setting a supported state requires the line and address to be in the proper state. A zero in a bit position indicates that the corresponding state is never available. A one indicates that the corresponding state may be available if the line is in the appropriate state for the state to be meaningful. This field allows an application to discover which agent states can be (and which can never be) supported on the device.


### -field dwMaxNumGroupEntries

Maximum number of agent identifiers that can be logged in on the address simultaneously. Determines the highest value that can be passed in as the <b>dwNumEntries</b> member in the 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a> structure to 
<a href="https://msdn.microsoft.com/ce6795fb-fe11-4125-abeb-9b2686ea669a">lineSetAgentGroup</a>.


### -field dwAgentStatusMessages

Indicates the 
<a href="https://msdn.microsoft.com/068a2b24-a430-4cf5-b70d-5574e981a899">LINEAGENTSTATUS_ constants</a> that can be received by the application in <i>dwParam2</i> of a 
<a href="https://msdn.microsoft.com/48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4">LINE_AGENTSTATUS</a> message.


### -field dwNumAgentExtensionIDs

Number of 
<a href="https://msdn.microsoft.com/bf7d9ccc-3f80-4e54-bcc2-cc2fef1d24af">LINEEXTENSIONID</a> structures that appear in the <i>ExtensionIDList</i> array. The value is 0 if agent-handler-specific extensions are supported on the address.


### -field dwAgentExtensionIDListSize

Size of the agent extension IDs array, in bytes.


### -field dwAgentExtensionIDListOffset

Offset from the beginning of the structure to an array of 
<a href="https://msdn.microsoft.com/bf7d9ccc-3f80-4e54-bcc2-cc2fef1d24af">LINEEXTENSIONID</a> structures. The size is <b>dwNumExtensionIDs</b> times SIZEOF(LINEEXTENSIONID). The array lists the 128-bit universally unique identifiers for all agent-handler-specific extensions supported by the agent handle for the address. The extension being used is referenced in the 
<a href="https://msdn.microsoft.com/4a1f2be4-4465-418a-9717-3857acf930a4">lineAgentSpecific</a> function and 
<a href="https://msdn.microsoft.com/67e1796c-02e5-4f81-8086-7c2ff3112ae0">LINE_AGENTSPECIFIC</a> message by its position in this table, the first entry being entry 0, so it is important that the agent handler always present extension identifiers in this array in the same order. The size of the array is specified by <b>dwAgentExtensionIDListOffset</b>.


### -field ProxyGUID

GUID for ACD proxy associated with the line. This element is exposed only to applications that negotiate a TAPI version of 2.2 or higher.


## -see-also




<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>



<a href="https://msdn.microsoft.com/bf7d9ccc-3f80-4e54-bcc2-cc2fef1d24af">LINEEXTENSIONID</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/67e1796c-02e5-4f81-8086-7c2ff3112ae0">LINE_AGENTSPECIFIC</a>



<a href="https://msdn.microsoft.com/48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4">LINE_AGENTSTATUS</a>



<a href="https://msdn.microsoft.com/4a1f2be4-4465-418a-9717-3857acf930a4">lineAgentSpecific</a>



<a href="https://msdn.microsoft.com/04bb6c00-2654-4707-ab11-2490ab5d9ab0">lineGetAgentCaps</a>



<a href="https://msdn.microsoft.com/ce6795fb-fe11-4125-abeb-9b2686ea669a">lineSetAgentGroup</a>



<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentState</a>
 

 

