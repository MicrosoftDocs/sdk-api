---
UID: NF:directmanipulation.IDirectManipulationDeferContactService.DeferContact
title: IDirectManipulationDeferContactService::DeferContact method
author: windows-driver-content
description: Specifies the amount of time to defer the execution of a call to SetContact for this pointerId.
old-location: directmanipulation\idirectmanipulationdefercontactservice_defercontact.htm
old-project: directmanipulation
ms.assetid: DEC97DD5-E43F-4541-8A80-D20EC8026493
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CancelContact method [Direct Manipulation], CancelContact method [Direct Manipulation], IDirectManipulationDeferContactService interface, DeferContact,IDirectManipulationDeferContactService.DeferContact, IDirectManipulationDeferContactService, IDirectManipulationDeferContactService interface [Direct Manipulation], CancelContact method, IDirectManipulationDeferContactService::CancelContact, IDirectManipulationDeferContactService::DeferContact, directmanipulation.idirectmanipulationdefercontactservice_defercontact, directmanipulation/IDirectManipulationDeferContactService::CancelContact
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationDeferContactService.CancelContact
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationDeferContactService::DeferContact method


## -description


Specifies the amount of time to defer the execution of a call to <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> for this <i>pointerId</i>.

<b>DeferContact</b> must be called before <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a>.


## -parameters




### -param pointerId [in]

The ID of the pointer.


### -param timeout [in]

The duration of the deferral, in milliseconds. The maximum value is 500.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a>
 

 

