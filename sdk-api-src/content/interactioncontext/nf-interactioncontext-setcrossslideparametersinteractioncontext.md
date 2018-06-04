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

# SetCrossSlideParametersInteractionContext function


## -description


Configures the cross-slide interaction. 


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


### -param parameterCount [in]

Number of parameters to set.


### -param crossSlideParameters [in]

The cross-slide threshold and its distance threshold.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



<b>SetCrossSlideParametersInteractionContext</b> fails if a <a href="https://msdn.microsoft.com/3871f24e-34a4-4524-801d-4d60cf6165d9">CROSS_SLIDE_PARAMETER</a> is enabled, but not specified  in the <i>crossSlideParameters</i> parameter.


#### Examples

This example demonstrates how to set custom cross-slide thresholds.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  SetCrossSlideParametersInteractionContext

CROSS_SLIDE_PARAMETER crossSlideParameters[4];
crossSlideParameters[0].threshold = CROSS_SLIDE_THRESHOLD_SELECT_START;
crossSlideParameters[0].distance = customSelectStart;
crossSlideParameters[1].threshold = CROSS_SLIDE_THRESHOLD_SPEED_BUMP_START;
crossSlideParameters[1].distance = customSpeedBumpStart;
crossSlideParameters[2].threshold = CROSS_SLIDE_THRESHOLD_SPEED_BUMP_END;
crossSlideParameters[2].distance = customSpeedBumpEnd;
crossSlideParameters[3].threshold = CROSS_SLIDE_THRESHOLD_REARRANGE_START;
crossSlideParameters[3].distance = customRearrangeStart;


// set thresholds for select, speedbump, and rearrange
SetCrossSlideParametersInteractionContext(
    m_interactionContext,
    4,
    crossSlideParameters);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3871f24e-34a4-4524-801d-4d60cf6165d9">CROSS_SLIDE_PARAMETER</a>



<a href="https://msdn.microsoft.com/19e934c6-8cd7-4302-a903-bd7865aef908">GetCrossSlideParameterInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

