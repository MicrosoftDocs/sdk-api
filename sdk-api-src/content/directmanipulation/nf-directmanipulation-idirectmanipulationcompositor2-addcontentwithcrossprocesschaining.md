---
UID: NF:directmanipulation.IDirectManipulationCompositor2.AddContentWithCrossProcessChaining
title: IDirectManipulationCompositor2::AddContentWithCrossProcessChaining
author: windows-sdk-content
description: Associates content (owned by the component host) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals.
old-location: directmanipulation\idirectmanipulationcompositor2_addcontentwithcrossprocesschaining.htm
old-project: directmanipulation
ms.assetid: dd6052df-30b5-4872-89a7-b98126fcd44d
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: AddContentWithCrossProcessChaining, AddContentWithCrossProcessChaining method [Direct Manipulation], AddContentWithCrossProcessChaining method [Direct Manipulation],IDirectManipulationCompositor2 interface, IDirectManipulationCompositor2 interface [Direct Manipulation],AddContentWithCrossProcessChaining method, IDirectManipulationCompositor2.AddContentWithCrossProcessChaining, IDirectManipulationCompositor2::AddContentWithCrossProcessChaining, directmanipulation.idirectmanipulationcompositor2_addcontentwithcrossprocesschaining, directmanipulation/IDirectManipulationCompositor2::AddContentWithCrossProcessChaining
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Directmanipulation.idl
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
 - directmanipulation.h
api_name:
 - IDirectManipulationCompositor2.AddContentWithCrossProcessChaining
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationCompositor2::AddContentWithCrossProcessChaining


## -description


Associates content (owned by the component host) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals. Represents a compositor object that associates manipulated content with drawing surfaces across multiple processes.


## -parameters




### -param content [in]

The content to add to the composition tree.

<i>content</i> is placed  between <i>parentVisual</i> and <i>childVisual</i> in the composition tree. 

Only primary content, created at the same time as the viewport, is valid.


### -param device [in]

The device used to compose the content. 

<div class="alert"><b>Note</b>  <i>device</i> is created by the application.</div>
<div> </div>

### -param parentVisual [in]

The parent visuals in the composition tree of the content being added.

<i>parentVisual</i> must also be a parent of <i>childVisual</i> in the composition tree.


### -param childVisual [in]

The child visuals in the composition tree of the content being added.

<i>parentVisual</i> must also be a parent of <i>childVisual</i> in the composition tree.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method inserts a small visual tree (owned by the <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> device) between the <i>parentVisual</i> and the <i>childVisual</i>. Transforms can then be applied to the inserted content.  


All content, regardless of type, must be added to the compositor. 

If the application uses a system-provided <a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>:

<ul>
<li><i>device</i> must be an  <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> object, and parent and child visuals must be <a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a> objects.</li>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> cannot be NULL. </li>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> objects are created and owned by the application.
</li>
<li>When content is added to the composition tree using this method, the new composition visuals are inserted between <i>parentVisual</i> and <i>childVisual</i>. The new visuals should not be destroyed until they are disassociated from the compositor with <a href="https://msdn.microsoft.com/9bfb7fe4-abf9-4bb7-8d3f-673508053573">RemoveContent</a>.</li>
</ul>
If the application uses a custom implementation of <a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>:

<ul>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> must be a valid type for the compositor. They do not have to be <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> or <a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a> objects.</li>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> can be NULL, depending on the compositor. </li>
</ul>
The cross-process pointer events (<a href="https://msdn.microsoft.com/06F8152C-0DA0-4820-835E-07AD35B24310">WM_POINTERROUTEDAWAY</a>, <a href="https://msdn.microsoft.com/B031ED80-6F1B-42A7-B4E2-55934E2C456C">WM_POINTERROUTEDRELEASED</a>, and <a href="https://msdn.microsoft.com/163E2C31-4E29-4CBA-B079-1963D4762D7B">WM_POINTERROUTEDTO</a>) should be handled appropriately. 




## -see-also




<a href="https://msdn.microsoft.com/e428ddaa-3913-498a-a3fd-bed10289cd8d">IDirectManipulationCompositor2</a>



<a href="https://msdn.microsoft.com/06F8152C-0DA0-4820-835E-07AD35B24310">WM_POINTERROUTEDAWAY</a>



<a href="https://msdn.microsoft.com/B031ED80-6F1B-42A7-B4E2-55934E2C456C">WM_POINTERROUTEDRELEASED</a>



<a href="https://msdn.microsoft.com/163E2C31-4E29-4CBA-B079-1963D4762D7B">WM_POINTERROUTEDTO</a>
 

 

