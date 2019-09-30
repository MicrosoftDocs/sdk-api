---
UID: NF:directmanipulation.IDirectManipulationViewport.GetStatus
title: IDirectManipulationViewport::GetStatus (directmanipulation.h)
author: windows-sdk-content
description: Gets the state of the viewport.
old-location: directmanipulation\idirectmanipulationviewport_getstatus.htm
tech.root: directmanipulation
ms.assetid: 1c02b2b2-8291-4151-b9c9-d80bf71f5ef5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Direct Manipulation], GetStatus method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],GetStatus method, IDirectManipulationViewport.GetStatus, IDirectManipulationViewport::GetStatus, directmanipulation.idirectmanipulationviewport_getstatus, directmanipulation/IDirectManipulationViewport::GetStatus
ms.topic: method
f1_keywords: 
 - "directmanipulation/IDirectManipulationViewport.GetStatus"
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
 - IDirectManipulationViewport.GetStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationViewport::GetStatus


## -description


Gets the state of the viewport.


## -parameters




### -param status [out, retval]

One of the values from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_status">DIRECTMANIPULATION_STATUS</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method returns the viewport state at the time of the call and not at the time when the return value is read.

This method will fail if called after <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-abandon">Abandon</a>.


#### Examples

The following example shows how to use this method.


```
DIRECTMANIPULATION_STATUS status;

HRESULT hr = pViewport->GetStatus(&status);

```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
 

 

