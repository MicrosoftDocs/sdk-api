---
UID: NF:directmanipulation.IDirectManipulationViewport.ReleaseContact
title: IDirectManipulationViewport::ReleaseContact
author: windows-sdk-content
description: Removes a contact that is associated with a viewport.
old-location: directmanipulation\idirectmanipulationviewport_releasecontact.htm
tech.root: directmanipulation
ms.assetid: fbb5cfba-4722-4470-aad5-2d192825244b
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],ReleaseContact method, IDirectManipulationViewport.ReleaseContact, IDirectManipulationViewport::ReleaseContact, ReleaseContact, ReleaseContact method [Direct Manipulation], ReleaseContact method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_releasecontact, directmanipulation/IDirectManipulationViewport::ReleaseContact
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.ReleaseContact
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::ReleaseContact


## -description


Removes a contact that is associated with a viewport.


## -parameters




### -param pointerId [in]

The ID of the pointer.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method releases a contact from a specific <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> viewport (equivalent to the user removing a touch point). 

The viewport state is not affected unless the last remaining contact on the viewport is removed, in which case the viewport will transition to inertia, if supported. 




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

