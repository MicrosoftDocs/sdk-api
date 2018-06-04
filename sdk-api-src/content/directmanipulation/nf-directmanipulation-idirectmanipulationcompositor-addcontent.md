---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDirectManipulationCompositor::AddContent


## -description


Associates content (owned by the caller) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals. 


## -parameters




### -param content [in]

The content to add to the composition tree.

<i>content</i> is placed  between <i>parentVisual</i> and <i>childVisual</i> in the composition tree. 


### -param device [in, optional]

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


All content, regardless of type, must be added to the compositor. This can be primary content, obtained from the viewport by calling <a href="https://msdn.microsoft.com/1aa70be3-9e95-4c35-8cca-45c1b238961e">GetPrimaryContent</a>, or secondary content, such as a panning indicator, created by calling <a href="https://msdn.microsoft.com/f8a2fbb2-f662-4eb7-88fb-64286205f19e">CreateContent</a>.


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



## -see-also




<a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>
 

 

