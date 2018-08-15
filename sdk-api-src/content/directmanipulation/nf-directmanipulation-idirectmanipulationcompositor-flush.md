---
UID: NF:directmanipulation.IDirectManipulationCompositor.Flush
title: IDirectManipulationCompositor::Flush
author: windows-sdk-content
description: Commits all pending updates in the compositor to the system for rendering.
old-location: directmanipulation\idirectmanipulationcompositor_flush.htm
old-project: directmanipulation
ms.assetid: E6D1BD41-6D5A-4BC0-983E-CBE79613FCF8
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: Flush, Flush method [Direct Manipulation], Flush method [Direct Manipulation],IDirectManipulationCompositor interface, IDirectManipulationCompositor interface [Direct Manipulation],Flush method, IDirectManipulationCompositor.Flush, IDirectManipulationCompositor::Flush, directmanipulation.idirectmanipulationcompositor_flush, directmanipulation/IDirectManipulationCompositor::Flush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.redist: 
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
 - IDirectManipulationCompositor.Flush
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationCompositor::Flush


## -description


Commits all pending updates in the compositor to the system for rendering.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method enables <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> to flush any pending changes to its visuals before a system event, such as a process suspension.




## -see-also




<a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>
 

 

