---
UID: NF:directmanipulation.IDirectManipulationDeferContactService.CancelContact
title: IDirectManipulationDeferContactService::CancelContact method
author: windows-driver-content
description: Cancel all scheduled calls to SetContact for this pointerId.
old-location: directmanipulation\idirectmanipulationdefercontactservice_cancelcontact.htm
old-project: directmanipulation
ms.assetid: 5C5029E5-CA4B-4853-B9D3-B99E869A44C3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CancelContact method [Direct Manipulation], CancelContact method [Direct Manipulation], IDirectManipulationDeferContactService interface, CancelContact,IDirectManipulationDeferContactService.CancelContact, IDirectManipulationDeferContactService, IDirectManipulationDeferContactService interface [Direct Manipulation], CancelContact method, IDirectManipulationDeferContactService::CancelContact, directmanipulation.idirectmanipulationdefercontactservice_cancelcontact, directmanipulation/IDirectManipulationDeferContactService::CancelContact
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

# IDirectManipulationDeferContactService::CancelContact method


## -description


Cancel all scheduled calls to <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> for this <i>pointerId</i>.   
     


## -parameters




### -param pointerId [in]

The ID of the pointer.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This function fails if the timeout specified in <a href="https://msdn.microsoft.com/DEC97DD5-E43F-4541-8A80-D20EC8026493">DeferContact</a> has already been reached.  




## -see-also




<a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a>
 

 

