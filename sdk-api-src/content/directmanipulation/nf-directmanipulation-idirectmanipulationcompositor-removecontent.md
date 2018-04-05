---
UID: NF:directmanipulation.IDirectManipulationCompositor.RemoveContent
title: IDirectManipulationCompositor::RemoveContent method
author: windows-driver-content
description: Removes content from the compositor.
old-location: directmanipulation\idirectmanipulationcompositor_removecontent.htm
old-project: directmanipulation
ms.assetid: 9bfb7fe4-abf9-4bb7-8d3f-673508053573
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDirectManipulationCompositor, IDirectManipulationCompositor interface [Direct Manipulation], RemoveContent method, IDirectManipulationCompositor::RemoveContent, RemoveContent method [Direct Manipulation], RemoveContent method [Direct Manipulation], IDirectManipulationCompositor interface, RemoveContent,IDirectManipulationCompositor.RemoveContent, directmanipulation.idirectmanipulationcompositor_removecontent, directmanipulation/IDirectManipulationCompositor::RemoveContent
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
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationCompositor.RemoveContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationCompositor::RemoveContent method


## -description


Removes content from the compositor.


## -parameters




### -param content [in]

The content to remove from the composition tree.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method removes content added with <a href="https://msdn.microsoft.com/16c1a911-43cb-4c18-9e29-12a69b715e6a">AddContent</a> and restores the original relationships between parent visuals and child visuals in the composition tree. In other words, <b>RemoveContent</b> undoes <b>AddContent</b>.




## -see-also




<a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>
 

 

