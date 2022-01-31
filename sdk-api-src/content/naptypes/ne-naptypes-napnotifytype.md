---
UID: NE:naptypes.tagNapNotifyType
title: NapNotifyType (naptypes.h)
description: Enumerates the types of service notifications sent by the NapAgent service.
helpviewer_keywords: ["NapNotifyType","NapNotifyType enumeration [NAP]","nap.napnotifytype","napNotifyTypeQuarState","napNotifyTypeServiceState","napNotifyTypeUnknown","naptypes/NapNotifyType","naptypes/napNotifyTypeQuarState","naptypes/napNotifyTypeServiceState","naptypes/napNotifyTypeUnknown"]
old-location: nap\napnotifytype.htm
tech.root: NAP
ms.assetid: dc573bff-9f28-4aa1-8787-e2a2dccf9859
ms.date: 12/05/2018
ms.keywords: NapNotifyType, NapNotifyType enumeration [NAP], nap.napnotifytype, napNotifyTypeQuarState, napNotifyTypeServiceState, napNotifyTypeUnknown, naptypes/NapNotifyType, naptypes/napNotifyTypeQuarState, naptypes/napNotifyTypeServiceState, naptypes/napNotifyTypeUnknown
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
req.typenames: NapNotifyType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNapNotifyType
 - naptypes/tagNapNotifyType
 - NapNotifyType
 - naptypes/NapNotifyType
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
 - NapNotifyType
---

# NapNotifyType enumeration


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>Enumerates the types of service notifications sent by the NapAgent service. The NapAgent is also known as the Quarantine Agent.

## -enum-fields

### -field napNotifyTypeUnknown:0

Not used.

### -field napNotifyTypeServiceState:1

NapAgent service state change notifications. 

A notification of type <b>napNotifyTypeServiceState</b> is sent whenever the NapAgent service stops or starts.

### -field napNotifyTypeQuarState:2

Quarantine state change notifications. 

A notification of type <b>napNotifyTypeQuarState</b>  is sent whenever the isolation state changes. For more information, see <a href="/windows/desktop/api/naptypes/ne-naptypes-isolationstate">IsolationState</a>.

## -see-also

<a href="/windows/desktop/NAP/initializenapagentnotifier">InitializeNapAgentNotifier</a>



<a href="/windows/desktop/NAP/uninitializenapagentnotifier">UninitializeNapAgentNotifier</a>
