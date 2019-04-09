---
UID: NF:directmanipulation.IDirectManipulationViewport.SetChaining
title: IDirectManipulationViewport::SetChaining (directmanipulation.h)
author: windows-sdk-content
description: Specifies the motion types supported in a viewport that can be chained to a parent viewport.
old-location: directmanipulation\idirectmanipulationviewport_setchaining.htm
tech.root: directmanipulation
ms.assetid: c172e985-4dc4-4d2a-a9e1-d88bc86ff75b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetChaining method, IDirectManipulationViewport.SetChaining, IDirectManipulationViewport::SetChaining, SetChaining, SetChaining method [Direct Manipulation], SetChaining method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setchaining, directmanipulation/IDirectManipulationViewport::SetChaining
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
 - IDirectManipulationViewport.SetChaining
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::SetChaining


## -description


Specifies the motion types supported in a viewport that can be chained to a parent viewport.


## -parameters




### -param enabledTypes [in]

One of the values from <a href="https://msdn.microsoft.com/a0b4da55-3ebb-4281-a372-4bc6b91e6789">DIRECTMANIPULATION_MOTION_TYPES</a> that specifies the motion types that are enabled for this viewport.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

