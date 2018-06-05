---
UID: NF:tuner.IAnalogTVTuningSpace.get_InputType
title: IAnalogTVTuningSpace::get_InputType
author: windows-sdk-content
description: The get_InputType method gets the input type (antenna or cable) intended for the tuning space.
old-location: mstv\ianalogtvtuningspace_get_inputtype.htm
old-project: mstv
ms.assetid: c016a61b-6b4f-4101-a357-38b8be754a57
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],get_InputType method, IAnalogTVTuningSpace.get_InputType, IAnalogTVTuningSpace::get_InputType, IAnalogTVTuningSpaceget_InputType, get_InputType, get_InputType method [Microsoft TV Technologies], get_InputType method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, mstv.ianalogtvtuningspace_get_inputtype, tuner/IAnalogTVTuningSpace::get_InputType
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IAnalogTVTuningSpace.get_InputType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogTVTuningSpace::get_InputType


## -description



The <b>get_InputType</b> method gets the input type (antenna or cable) intended for the tuning space.




## -parameters




### -param InputTypeVal






#### - pInputTypeVal [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/e25ec8e2-6d94-4059-a34e-a9e7887582fb">TunerInputType</a> that receives the input type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace Interface</a>
 

 

