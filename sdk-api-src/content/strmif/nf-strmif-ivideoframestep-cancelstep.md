---
UID: NF:strmif.IVideoFrameStep.CancelStep
title: IVideoFrameStep::CancelStep (strmif.h)
description: The CancelStep method cancels the previous IVideoFrameStep::Step operation.
helpviewer_keywords: ["CancelStep","CancelStep method [DirectShow]","CancelStep method [DirectShow]","IVideoFrameStep interface","IVideoFrameStep interface [DirectShow]","CancelStep method","IVideoFrameStep.CancelStep","IVideoFrameStep::CancelStep","IVideoFrameStepCancelStep","dshow.ivideoframestep_cancelstep","strmif/IVideoFrameStep::CancelStep"]
old-location: dshow\ivideoframestep_cancelstep.htm
tech.root: dshow
ms.assetid: 1310d4d8-a1a3-493c-baee-f7c0ec5790e1
ms.date: 12/05/2018
ms.keywords: CancelStep, CancelStep method [DirectShow], CancelStep method [DirectShow],IVideoFrameStep interface, IVideoFrameStep interface [DirectShow],CancelStep method, IVideoFrameStep.CancelStep, IVideoFrameStep::CancelStep, IVideoFrameStepCancelStep, dshow.ivideoframestep_cancelstep, strmif/IVideoFrameStep::CancelStep
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVideoFrameStep::CancelStep
 - strmif/IVideoFrameStep::CancelStep
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoFrameStep.CancelStep
---

# IVideoFrameStep::CancelStep


## -description

The <code>CancelStep</code> method cancels the previous <a href="/windows/desktop/api/strmif/nf-strmif-ivideoframestep-step">IVideoFrameStep::Step</a> operation.



## -returns

Returns S_OK if the <b>Step</b> operation was successfully canceled, or E_FAIL otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivideoframestep">IVideoFrameStep Interface</a>
