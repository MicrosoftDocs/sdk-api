---
UID: NS:naptypes.tagSystemHealthAgentState
title: tagSystemHealthAgentState
author: windows-sdk-content
description: Stores the dynamic state of the SHA.
old-location: nap\systemhealthagentstate_struct.htm
tech.root: NAP
ms.assetid: c5a5bc72-363d-4c2d-8b91-fda64fac281e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SystemHealthAgentState, SystemHealthAgentState structure [NAP], nap.systemhealthagentstate_struct, naptypes/SystemHealthAgentState, tagSystemHealthAgentState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - SystemHealthAgentState
product: Windows
targetos: Windows
req.typenames: SystemHealthAgentState
req.redist: 
---

# tagSystemHealthAgentState structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>SystemHealthAgentState</b> structure stores the dynamic state of the SHA.


## -struct-fields




### -field id

A unique <a href="https://msdn.microsoft.com/54f2866b-4333-4fc8-bb25-b7d4ae72b7dc">SystemHealthEntityId</a> value that identifies the System Health Agent (SHA).


### -field shaResultCodes

A <a href="https://msdn.microsoft.com/9d608f0a-9841-48e6-8856-2d8c1afc3e5d">ResultCodes</a> structure that contains the compliance result codes that were returned in the most recent <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHRespnse</a> received from the SHA.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/ba725bf1-1d0a-4489-b912-3e761557d772">sohAttributeTypeComplianceResultCodes</a> attribute type within the <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHRespnse</a> contains the compliance result codes.</div>
<div> </div>

### -field failureCategory

A <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">FailureCategory</a> value that describes the failure category fields that were returned in the most recent <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHRespnse</a> received from the SHA.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/ba725bf1-1d0a-4489-b912-3e761557d772">sohAttributeTypeFailureCategory</a> attribute type within the <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHRespnse</a> contains the failure category fields.</div>
<div> </div>

### -field fixupInfo

A <a href="https://msdn.microsoft.com/8f91534e-3281-4d5a-9af7-5f08eb0243f0">FixupInfo</a> structure that contains information about the fix-up state of the SHA.


## -see-also




<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 

