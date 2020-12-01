---
UID: NF:manipulations.IInertiaProcessor.Process
title: IInertiaProcessor::Process (manipulations.h)
description: The Process method performs calculations and can raise the Started, Delta, or Completed event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op.
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","Process method","IInertiaProcessor.Process","IInertiaProcessor::Process","Process","Process method [Windows Touch]","Process method [Windows Touch]","IInertiaProcessor interface","manipulations/IInertiaProcessor::Process","wintouch.iinertiaprocessor_process"]
old-location: wintouch\iinertiaprocessor_process.htm
tech.root: wintouch
ms.assetid: f63cafa0-0da6-46ba-91d3-956dc804dd79
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],Process method, IInertiaProcessor.Process, IInertiaProcessor::Process, Process, Process method [Windows Touch], Process method [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::Process, wintouch.iinertiaprocessor_process
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
 - IInertiaProcessor::Process
 - manipulations/IInertiaProcessor::Process
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
 - IInertiaProcessor.Process
---

# IInertiaProcessor::Process


## -description

The <b>Process</b> method performs calculations and can raise the <b>Started</b>, <b>Delta</b>, or <b>Completed</b> event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op.

## -parameters

### -param completed [out]

Indicates whether an operation was performed. A value of false indicates extrapolation was finished at a previous tick and the operation was a no-op.

## -returns

Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/imanipulationprocessor-methods">Methods</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime">ProcessTime</a>