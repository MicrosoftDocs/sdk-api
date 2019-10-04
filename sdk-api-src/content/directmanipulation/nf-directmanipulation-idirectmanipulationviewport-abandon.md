---
UID: NF:directmanipulation.IDirectManipulationViewport.Abandon
title: IDirectManipulationViewport::Abandon (directmanipulation.h)
author: windows-sdk-content
description: Releases all resources that are used by the viewport and prepares it for destruction from memory.
old-location: directmanipulation\idirectmanipulationviewport_abandon.htm
tech.root: directmanipulation
ms.assetid: 83d0bcde-03d2-4eba-991a-399b5307c8bd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Abandon, Abandon method [Direct Manipulation], Abandon method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],Abandon method, IDirectManipulationViewport.Abandon, IDirectManipulationViewport::Abandon, directmanipulation.idirectmanipulationviewport_abandon, directmanipulation/IDirectManipulationViewport::Abandon
ms.topic: method
f1_keywords: 
 - "directmanipulation/IDirectManipulationViewport.Abandon"
dev_langs:
 - c++
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
 - IDirectManipulationViewport.Abandon
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationViewport::Abandon


## -description


    Releases all resources that are used by the viewport and prepares it for destruction from memory.



## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Once <b>Abandon</b> has been called, do not make subsequent function calls on the viewport. If a function is called after <b>Abandon</b>, <b>E_INVALID_STATE</b> will be returned.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
 

 

