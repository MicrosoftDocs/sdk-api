---
UID: NF:tuner.IAnalogTVTuningSpace.put_InputType
title: IAnalogTVTuningSpace::put_InputType
author: windows-driver-content
description: The put_InputType method sets the input type (antenna or cable) intended for the tuning space.
old-location: mstv\ianalogtvtuningspace_put_inputtype.htm
old-project: mstv
ms.assetid: 399503a2-60e9-4feb-ba69-cafef70b2540
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],put_InputType method, IAnalogTVTuningSpace.put_InputType, IAnalogTVTuningSpace::put_InputType, IAnalogTVTuningSpaceput_InputType, mstv.ianalogtvtuningspace_put_inputtype, put_InputType, put_InputType method [Microsoft TV Technologies], put_InputType method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, tuner/IAnalogTVTuningSpace::put_InputType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IAnalogTVTuningSpace.put_InputType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogTVTuningSpace::put_InputType


## -description



The <b>put_InputType</b> method sets the input type (antenna or cable) intended for the tuning space.




## -parameters




### -param NewInputTypeVal [in]

Variable of type <a href="https://msdn.microsoft.com/e25ec8e2-6d94-4059-a34e-a9e7887582fb">TunerInputType</a> that specifies the input type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace Interface</a>
 

 

