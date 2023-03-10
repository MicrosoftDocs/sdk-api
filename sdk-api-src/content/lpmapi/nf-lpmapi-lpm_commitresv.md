---
UID: NF:lpmapi.LPM_CommitResv
title: LPM_CommitResv function (lpmapi.h)
description: The LPM_CommitResv function is called by the PCM to obtain reservation commitment decisions from the LPM.
helpviewer_keywords: ["LPM_CommitResv","LPM_CommitResv callback","LPM_CommitResv callback function [QOS]","RESOURCES_ALLOCATED","RESOURCES_MODIFIED","_gqos_lpm_commitresv","lpmapi/LPM_CommitResv","qos.lpm_commitresv"]
old-location: qos\lpm_commitresv.htm
tech.root: QOS
ms.assetid: 3a04e96d-d91e-47de-9958-75fbd32cba6b
ms.date: 12/05/2018
ms.keywords: LPM_CommitResv, LPM_CommitResv callback, LPM_CommitResv callback function [QOS], RESOURCES_ALLOCATED, RESOURCES_MODIFIED, _gqos_lpm_commitresv, lpmapi/LPM_CommitResv, qos.lpm_commitresv
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPM_CommitResv
 - lpmapi/LPM_CommitResv
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - LPM_CommitResv
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
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure installed on the specified interface. The 
<b>FLOWSPEC</b> structure is a merged flow for all receivers that can be reached by <i>FlowInstalledIntf</i>.

### -param CommitDecision [in]

Value of the commitment decision reached by the LPM. The following list indicates possible values:

<a id="RESOURCES_ALLOCATED"></a>
<a id="resources_allocated"></a>


#### RESOURCES_ALLOCATED

<a id="RESOURCES_MODIFIED"></a>
<a id="resources_modified"></a>


#### RESOURCES_MODIFIED

## -remarks

When the resources are allocated by the SBM for a new reservation, it calls LPMs with <i>CommitDecision</i> set to RESOURCES_ALLOCATED. When resources allocated for an existing reservation are changed, the SBM calls the 
<i>LPM_CommitResv</i> function with <i>CommitDecision</i> set to RESOURCES_MODIFIED.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>