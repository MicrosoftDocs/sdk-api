---
UID: NS:naptypes.tagSystemHealthAgentState
title: SystemHealthAgentState (naptypes.h)
description: Stores the dynamic state of the SHA.
helpviewer_keywords: ["SystemHealthAgentState","SystemHealthAgentState structure [NAP]","nap.systemhealthagentstate_struct","naptypes/SystemHealthAgentState"]
old-location: nap\systemhealthagentstate_struct.htm
tech.root: NAP
ms.assetid: c5a5bc72-363d-4c2d-8b91-fda64fac281e
ms.date: 12/05/2018
ms.keywords: SystemHealthAgentState, SystemHealthAgentState structure [NAP], nap.systemhealthagentstate_struct, naptypes/SystemHealthAgentState
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
targetos: Windows
req.typenames: SystemHealthAgentState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSystemHealthAgentState
 - naptypes/tagSystemHealthAgentState
 - SystemHealthAgentState
 - naptypes/SystemHealthAgentState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - SystemHealthAgentState
---

# SystemHealthAgentState structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>SystemHealthAgentState</b> structure stores the dynamic state of the SHA.

## -struct-fields

### -field id

A unique <a href="/windows/desktop/NAP/nap-datatypes">SystemHealthEntityId</a> value that identifies the System Health Agent (SHA).

### -field shaResultCodes

A <a href="/windows/desktop/api/naptypes/ns-naptypes-resultcodes">ResultCodes</a> structure that contains the compliance result codes that were returned in the most recent <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHRespnse</a> received from the SHA.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/NAP/sohattributetype-enum">sohAttributeTypeComplianceResultCodes</a> attribute type within the <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHRespnse</a> contains the compliance result codes.</div>
<div> </div>

### -field failureCategory

A <a href="/windows/desktop/api/naptypes/ne-naptypes-failurecategory">FailureCategory</a> value that describes the failure category fields that were returned in the most recent <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHRespnse</a> received from the SHA.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/NAP/sohattributetype-enum">sohAttributeTypeFailureCategory</a> attribute type within the <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHRespnse</a> contains the failure category fields.</div>
<div> </div>

### -field fixupInfo

A <a href="/windows/desktop/api/naptypes/ns-naptypes-fixupinfo">FixupInfo</a> structure that contains information about the fix-up state of the SHA.

## -see-also

<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>