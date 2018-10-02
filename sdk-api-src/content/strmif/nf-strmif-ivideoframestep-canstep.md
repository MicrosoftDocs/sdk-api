---
UID: NF:strmif.IVideoFrameStep.CanStep
title: IVideoFrameStep::CanStep
author: windows-sdk-content
description: The CanStep method determines the stepping capabilities of the specified filter.
old-location: dshow\ivideoframestep_canstep.htm
tech.root: DirectShow
ms.assetid: e2e3f665-28be-4a6d-b29a-4f0485d9a672
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CanStep, CanStep method [DirectShow], CanStep method [DirectShow],IVideoFrameStep interface, IVideoFrameStep interface [DirectShow],CanStep method, IVideoFrameStep.CanStep, IVideoFrameStep::CanStep, IVideoFrameStepCanStep, dshow.ivideoframestep_canstep, strmif/IVideoFrameStep::CanStep
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoFrameStep::CanStep


## -description



The <code>CanStep</code> method determines the stepping capabilities of the specified filter.




## -parameters




### -param bMultiple

If <i>bMultiple</i> is zero and the method returns S_OK, the graph can step one frame at a time. If <i>bMultiple</i> if greater than zero and the method returns S_OK, the graph can step <i>bMultiple</i> frames at a time.


### -param pStepObject

Pointer to an interface on the filter that will control the stepping operation. Specify <b>NULL</b> to perform frame stepping using the renderer filter in the graph. If the graph includes a custom filter that implements the frame stepping, then <i>pStepObject</i> should specify that filter's <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface.


## -returns



Returns S_OK if the object can step or E_INVALIDARG if <i>pStepObject</i> is invalid.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7bf45473-144c-49f8-8178-aff5b60112b6">IVideoFrameStep Interface</a>
 

 

