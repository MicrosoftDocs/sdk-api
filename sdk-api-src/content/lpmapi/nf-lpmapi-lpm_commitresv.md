---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# LPM_CommitResv function


## -description


The 
<i>LPM_CommitResv</i> function is called by the PCM to obtain reservation commitment decisions from the LPM.


## -parameters




### -param RsvpSession [in]

Pointer to the RSVP session object for which the reservation commitment is being requested.


### -param FlowInstalledIntf [in]

Pointer to the interface on which the message was received. The received interface IP address is supplied as the RSVP HOP object, and the Logical Interface Handle is set to the SNMP Index. Note that interface index numbers can change with the addition and deletion of interfaces, due to the Plug and Play features of Windows 2000.


### -param RsvpStyle [in]

RSVP reservation style being requested.


### -param FilterSpecCount [in]

Number of filter specs in <i>ppFilterSpecList</i>.


### -param ppFilterSpecList [in]

Array of filter specs, listing the senders for whom the flow is created.


### -param pMergedFlowSpec [in]

The 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure installed on the specified interface. The 
<b>FLOWSPEC</b> structure is a merged flow for all receivers that can be reached by <i>FlowInstalledIntf</i>.


### -param CommitDecision [in]

Value of the commitment decision reached by the LPM. The following list indicates possible values:

<a id="RESOURCES_ALLOCATED"></a>
<a id="resources_allocated"></a>


#### RESOURCES_ALLOCATED

<a id="RESOURCES_MODIFIED"></a>
<a id="resources_modified"></a>


#### RESOURCES_MODIFIED


## -returns



This callback function does not return a value.




## -remarks



When the resources are allocated by the SBM for a new reservation, it calls LPMs with <i>CommitDecision</i> set to RESOURCES_ALLOCATED. When resources allocated for an existing reservation are changed, the SBM calls the 
<i>LPM_CommitResv</i> function with <i>CommitDecision</i> set to RESOURCES_MODIFIED.




## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>
 

 

