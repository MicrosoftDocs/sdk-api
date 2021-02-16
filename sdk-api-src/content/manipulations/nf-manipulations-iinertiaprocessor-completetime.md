---
UID: NF:manipulations.IInertiaProcessor.CompleteTime
title: IInertiaProcessor::CompleteTime (manipulations.h)
description: Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.
helpviewer_keywords: ["CompleteTime","CompleteTime method [Windows Touch]","CompleteTime method [Windows Touch]","IInertiaProcessor interface","IInertiaProcessor interface [Windows Touch]","CompleteTime method","IInertiaProcessor.CompleteTime","IInertiaProcessor::CompleteTime","manipulations/IInertiaProcessor::CompleteTime","wintouch.iinertiaprocessor_completetime"]
old-location: wintouch\iinertiaprocessor_completetime.htm
tech.root: wintouch
ms.assetid: 325e04c2-a477-43c7-9513-36a2a92eef8e
ms.date: 12/05/2018
ms.keywords: CompleteTime, CompleteTime method [Windows Touch], CompleteTime method [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],CompleteTime method, IInertiaProcessor.CompleteTime, IInertiaProcessor::CompleteTime, manipulations/IInertiaProcessor::CompleteTime, wintouch.iinertiaprocessor_completetime
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
 - IInertiaProcessor::CompleteTime
 - manipulations/IInertiaProcessor::CompleteTime
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
 - IInertiaProcessor.CompleteTime
---

# IInertiaProcessor::CompleteTime


## -description

Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event.

## -parameters

### -param timestamp [in]

A parameter containing a timestamp (in milliseconds) to process.

## -returns

Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.

## -remarks

The <b>CompleteTime</b> method raises the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event on an <a href="/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents">_IManipulationEvents</a> interface implementation.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete">Complete</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/imanipulationprocessor-methods">Methods</a>