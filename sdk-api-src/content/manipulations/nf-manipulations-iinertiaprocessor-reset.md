---
UID: NF:manipulations.IInertiaProcessor.Reset
title: IInertiaProcessor::Reset (manipulations.h)
description: The Reset method initializes the processor with initial timestamp and restarts inertia.
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","Reset method","IInertiaProcessor.Reset","IInertiaProcessor::Reset","Reset","Reset method [Windows Touch]","Reset method [Windows Touch]","IInertiaProcessor interface","manipulations/IInertiaProcessor::Reset","wintouch.iinertiaprocessor_reset"]
old-location: wintouch\iinertiaprocessor_reset.htm
tech.root: wintouch
ms.assetid: 69ce260d-0674-4ff0-8610-bc814976bd3d
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],Reset method, IInertiaProcessor.Reset, IInertiaProcessor::Reset, Reset, Reset method [Windows Touch], Reset method [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::Reset, wintouch.iinertiaprocessor_reset
req.header: manipulations.h
req.include-header: Manipulations.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IInertiaProcessor::Reset
 - manipulations/IInertiaProcessor::Reset
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
 - IInertiaProcessor.Reset
---

# IInertiaProcessor::Reset


## -description

The <b>Reset</b> method initializes the processor with initial timestamp and restarts inertia.



## -returns

Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.

## -remarks

If you have changed properties on an object currently being manipulated by inertia, call <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete">Complete</a> before calling <b>Reset</b>.
	 


#### Examples


```cpp

    // set properties on the IInertiaProcessor interface
    this->m_spIInertProc->put_DesiredRotation(spin);    
	 
    // complete any unprocessed inertia
    this->m_spIInertProc->Complete();
	 
    // reset the processor
    this->m_spIInertProc->Reset();		  
	 
    // If you have implemented a timer that handles inertia processing,
    // this should be started as well and the processor will raise
    // Manipulation* events
		  
```

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete">Complete</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/imanipulationprocessor-methods">Methods</a>
