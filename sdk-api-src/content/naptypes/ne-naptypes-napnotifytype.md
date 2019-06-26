---
UID: NE:naptypes.tagNapNotifyType
title: NapNotifyType (naptypes.h)
author: windows-sdk-content
description: Enumerates the types of service notifications sent by the NapAgent service.
old-location: nap\napnotifytype.htm
tech.root: NAP
ms.assetid: dc573bff-9f28-4aa1-8787-e2a2dccf9859
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NapNotifyType, NapNotifyType enumeration [NAP], nap.napnotifytype, napNotifyTypeQuarState, napNotifyTypeServiceState, napNotifyTypeUnknown, naptypes/NapNotifyType, naptypes/napNotifyTypeQuarState, naptypes/napNotifyTypeServiceState, naptypes/napNotifyTypeUnknown
ms.topic: enum
f1_keywords: 
 - "naptypes/NapNotifyType"
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
 - NapNotifyType
product: Windows
targetos: Windows
req.typenames: NapNotifyType
req.redist: 
ms.custom: 19H1
---

# NapNotifyType enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>Enumerates the types of service notifications sent by the NapAgent service. The NapAgent is also known as the Quarantine Agent.


## -enum-fields




### -field napNotifyTypeUnknown

Not used.


### -field napNotifyTypeServiceState

NapAgent service state change notifications. 

A notification of type <b>napNotifyTypeServiceState</b> is sent whenever the NapAgent service stops or starts.


### -field napNotifyTypeQuarState

Quarantine state change notifications. 

A notification of type <b>napNotifyTypeQuarState</b>  is sent whenever the isolation state changes. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ne-naptypes-tagisolationstate">IsolationState</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/NAP/initializenapagentnotifier">InitializeNapAgentNotifier</a>



<a href="https://docs.microsoft.com/windows/desktop/NAP/uninitializenapagentnotifier">UninitializeNapAgentNotifier</a>
 

 

