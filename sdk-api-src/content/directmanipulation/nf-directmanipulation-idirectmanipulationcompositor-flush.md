---
UID: NF:directmanipulation.IDirectManipulationCompositor.Flush
title: IDirectManipulationCompositor::Flush (directmanipulation.h)
author: windows-sdk-content
description: Commits all pending updates in the compositor to the system for rendering.
old-location: directmanipulation\idirectmanipulationcompositor_flush.htm
tech.root: directmanipulation
ms.assetid: E6D1BD41-6D5A-4BC0-983E-CBE79613FCF8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [Direct Manipulation], Flush method [Direct Manipulation],IDirectManipulationCompositor interface, IDirectManipulationCompositor interface [Direct Manipulation],Flush method, IDirectManipulationCompositor.Flush, IDirectManipulationCompositor::Flush, directmanipulation.idirectmanipulationcompositor_flush, directmanipulation/IDirectManipulationCompositor::Flush
ms.topic: method
f1_keywords: 
 - "directmanipulation/IDirectManipulationCompositor.Flush"
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
 - IDirectManipulationCompositor.Flush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationCompositor::Flush


## -description


Commits all pending updates in the compositor to the system for rendering.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method enables <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> to flush any pending changes to its visuals before a system event, such as a process suspension.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>
 

 

