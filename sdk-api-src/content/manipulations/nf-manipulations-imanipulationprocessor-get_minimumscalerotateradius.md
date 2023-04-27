---
UID: NF:manipulations.IManipulationProcessor.get_MinimumScaleRotateRadius
title: IManipulationProcessor::get_MinimumScaleRotateRadius (manipulations.h)
description: Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation. (Get)
helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","MinimumScaleRotateRadius property","IManipulationProcessor.MinimumScaleRotateRadius","IManipulationProcessor.get_MinimumScaleRotateRadius","IManipulationProcessor::MinimumScaleRotateRadius","IManipulationProcessor::get_MinimumScaleRotateRadius","IManipulationProcessor::put_MinimumScaleRotateRadius","MinimumScaleRotateRadius property [Windows Touch]","MinimumScaleRotateRadius property [Windows Touch]","IManipulationProcessor interface","get_MinimumScaleRotateRadius","manipulations/IManipulationProcessor::MinimumScaleRotateRadius","manipulations/IManipulationProcessor::get_MinimumScaleRotateRadius","manipulations/IManipulationProcessor::put_MinimumScaleRotateRadius","wintouch.imanipulationprocessor_minimumscalerotateradius"]
old-location: wintouch\imanipulationprocessor_minimumscalerotateradius.htm
tech.root: wintouch
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],MinimumScaleRotateRadius property, IManipulationProcessor.MinimumScaleRotateRadius, IManipulationProcessor.get_MinimumScaleRotateRadius, IManipulationProcessor::MinimumScaleRotateRadius, IManipulationProcessor::get_MinimumScaleRotateRadius, IManipulationProcessor::put_MinimumScaleRotateRadius, MinimumScaleRotateRadius property [Windows Touch], MinimumScaleRotateRadius property [Windows Touch],IManipulationProcessor interface, get_MinimumScaleRotateRadius, manipulations/IManipulationProcessor::MinimumScaleRotateRadius, manipulations/IManipulationProcessor::get_MinimumScaleRotateRadius, manipulations/IManipulationProcessor::put_MinimumScaleRotateRadius, wintouch.imanipulationprocessor_minimumscalerotateradius
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IManipulationProcessor::get_MinimumScaleRotateRadius
 - manipulations/IManipulationProcessor::get_MinimumScaleRotateRadius
dev_langs:
 - c++
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
---

# IManipulationProcessor::get_MinimumScaleRotateRadius


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


```cpp
pManip->put_MinimumScaleRotateRadius(4000.0f);  

```

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>
