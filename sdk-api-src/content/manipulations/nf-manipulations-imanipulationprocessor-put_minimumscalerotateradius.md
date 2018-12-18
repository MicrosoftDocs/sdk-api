---
UID: NF:manipulations.IManipulationProcessor.put_MinimumScaleRotateRadius
title: IManipulationProcessor::put_MinimumScaleRotateRadius
author: windows-sdk-content
description: Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.
old-location: wintouch\imanipulationprocessor_minimumscalerotateradius.htm
tech.root: wintouch
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],MinimumScaleRotateRadius property, IManipulationProcessor.MinimumScaleRotateRadius, IManipulationProcessor.put_MinimumScaleRotateRadius, IManipulationProcessor::MinimumScaleRotateRadius, IManipulationProcessor::get_MinimumScaleRotateRadius, IManipulationProcessor::put_MinimumScaleRotateRadius, MinimumScaleRotateRadius property [Windows Touch], MinimumScaleRotateRadius property [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::MinimumScaleRotateRadius, manipulations/IManipulationProcessor::get_MinimumScaleRotateRadius, manipulations/IManipulationProcessor::put_MinimumScaleRotateRadius, put_MinimumScaleRotateRadius, wintouch.imanipulationprocessor_minimumscalerotateradius
ms.topic: method
req.header: manipulations.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IManipulationProcessor.MinimumScaleRotateRadius
 - IManipulationProcessor.get_MinimumScaleRotateRadius
 - IManipulationProcessor.put_MinimumScaleRotateRadius
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor::put_MinimumScaleRotateRadius


## -description


Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.
    

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is set in centipixels (100ths of a pixel).
  </div>
<div> </div>
    
	 Setting this value will make the manipulation processor ignore gestures that have too small of a radius.
	 This is useful if you want to prevent a user from manipulating an object to too small of a radius.  For example,
	 if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater
	 than 100 pixels, you would set this value to 10000.	
  


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>pManip-&gt;put_MinimumScaleRotateRadius(4000.0f);  
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>
 

 

