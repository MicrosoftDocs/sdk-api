---
UID: NF:strmif.IVideoFrameStep.CanStep
title: IVideoFrameStep::CanStep (strmif.h)
description: The CanStep method determines the stepping capabilities of the specified filter.
helpviewer_keywords: ["CanStep","CanStep method [DirectShow]","CanStep method [DirectShow]","IVideoFrameStep interface","IVideoFrameStep interface [DirectShow]","CanStep method","IVideoFrameStep.CanStep","IVideoFrameStep::CanStep","IVideoFrameStepCanStep","dshow.ivideoframestep_canstep","strmif/IVideoFrameStep::CanStep"]
old-location: dshow\ivideoframestep_canstep.htm
tech.root: dshow
ms.assetid: e2e3f665-28be-4a6d-b29a-4f0485d9a672
ms.date: 12/05/2018
ms.keywords: CanStep, CanStep method [DirectShow], CanStep method [DirectShow],IVideoFrameStep interface, IVideoFrameStep interface [DirectShow],CanStep method, IVideoFrameStep.CanStep, IVideoFrameStep::CanStep, IVideoFrameStepCanStep, dshow.ivideoframestep_canstep, strmif/IVideoFrameStep::CanStep
f1_keywords:
- strmif/IVideoFrameStep.CanStep
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVideoFrameStep.CanStep
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoFrameStep::CanStep


## -description



The <code>CanStep</code> method determines the stepping capabilities of the specified filter.




## -parameters




### -param bMultiple

If <i>bMultiple</i> is zero and the method returns S_OK, the graph can step one frame at a time. If <i>bMultiple</i> if greater than zero and the method returns S_OK, the graph can step <i>bMultiple</i> frames at a time.


### -param pStepObject

Pointer to an interface on the filter that will control the stepping operation. Specify <b>NULL</b> to perform frame stepping using the renderer filter in the graph. If the graph includes a custom filter that implements the frame stepping, then <i>pStepObject</i> should specify that filter's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface.


## -returns



Returns S_OK if the object can step or E_INVALIDARG if <i>pStepObject</i> is invalid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivideoframestep">IVideoFrameStep Interface</a>
 

 

