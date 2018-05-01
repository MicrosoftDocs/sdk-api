---
UID: NE:naptypes.tagNapNotifyType
title: tagNapNotifyType
author: windows-driver-content
description: Enumerates the types of service notifications sent by the NapAgent service.
old-location: nap\napnotifytype.htm
old-project: NAP
ms.assetid: dc573bff-9f28-4aa1-8787-e2a2dccf9859
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: NapNotifyType, NapNotifyType enumeration [NAP], nap.napnotifytype, napNotifyTypeQuarState, napNotifyTypeServiceState, napNotifyTypeUnknown, naptypes/NapNotifyType, naptypes/napNotifyTypeQuarState, naptypes/napNotifyTypeServiceState, naptypes/napNotifyTypeUnknown, tagNapNotifyType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadMUILibraryW (Unicode) and LoadMUILibraryA (ANSI)
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NapNotifyType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	NapTypes.h
api_name:
-	NapNotifyType
product: Windows
targetos: Windows
req.lib: Muiload.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# tagNapNotifyType enumeration


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

A notification of type <b>napNotifyTypeQuarState</b>  is sent whenever the isolation state changes. For more information, see <a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">IsolationState</a>.


## -see-also




<a href="https://msdn.microsoft.com/24180194-50d7-4f54-845d-25402af9cf9a">InitializeNapAgentNotifier</a>



<a href="https://msdn.microsoft.com/b676ee33-caf6-48f0-acf8-5be1b23c62fe">UninitializeNapAgentNotifier</a>
 

 

