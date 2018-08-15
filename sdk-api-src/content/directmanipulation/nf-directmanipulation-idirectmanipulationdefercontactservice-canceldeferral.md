---
UID: NF:directmanipulation.IDirectManipulationDeferContactService.CancelDeferral
title: IDirectManipulationDeferContactService::CancelDeferral
author: windows-sdk-content
description: Cancel the deferral set in DeferContact and process the scheduled SetContact call for this pointerId.
old-location: directmanipulation\idirectmanipulationdefercontactservice_canceldeferral.htm
old-project: directmanipulation
ms.assetid: 946F8CF8-6A6D-4BC1-B9BA-91D5B4A8A178
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CancelDeferral, CancelDeferral method [Direct Manipulation], CancelDeferral method [Direct Manipulation],IDirectManipulationDeferContactService interface, IDirectManipulationDeferContactService interface [Direct Manipulation],CancelDeferral method, IDirectManipulationDeferContactService.CancelDeferral, IDirectManipulationDeferContactService::CancelDeferral, directmanipulation.idirectmanipulationdefercontactservice_canceldeferral, directmanipulation/IDirectManipulationDeferContactService::CancelDeferral
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationDeferContactService.CancelDeferral
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationDeferContactService::CancelDeferral


## -description


Cancel the deferral set in <a href="https://msdn.microsoft.com/DEC97DD5-E43F-4541-8A80-D20EC8026493">DeferContact</a> and process the scheduled <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> call for this <i>pointerId</i>.   
     


## -parameters




### -param pointerId [in]

The ID of the pointer.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a>
 

 

