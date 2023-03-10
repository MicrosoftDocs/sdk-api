---
UID: NF:winsatcominterfacei.IWinSATInitiateEvents.WinSATUpdate
title: IWinSATInitiateEvents::WinSATUpdate (winsatcominterfacei.h)
description: Receives notification when an assessment is making progress.
helpviewer_keywords: ["IWinSATInitiateEvents interface [WinSAT]","WinSATUpdate method","IWinSATInitiateEvents.WinSATUpdate","IWinSATInitiateEvents::WinSATUpdate","WinSATUpdate","WinSATUpdate method [WinSAT]","WinSATUpdate method [WinSAT]","IWinSATInitiateEvents interface","winsat.iwinsatinitiateevents_winsatupdate","winsatcominterfacei/IWinSATInitiateEvents::WinSATUpdate"]
old-location: winsat\iwinsatinitiateevents_winsatupdate.htm
tech.root: WinSAT
ms.assetid: d0f527a9-89b9-45d6-b5a5-82b0ae1ad122
ms.date: 12/05/2018
ms.keywords: IWinSATInitiateEvents interface [WinSAT],WinSATUpdate method, IWinSATInitiateEvents.WinSATUpdate, IWinSATInitiateEvents::WinSATUpdate, WinSATUpdate, WinSATUpdate method [WinSAT], WinSATUpdate method [WinSAT],IWinSATInitiateEvents interface, winsat.iwinsatinitiateevents_winsatupdate, winsatcominterfacei/IWinSATInitiateEvents::WinSATUpdate
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Winsatapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWinSATInitiateEvents::WinSATUpdate
 - winsatcominterfacei/IWinSATInitiateEvents::WinSATUpdate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IWinSATInitiateEvents.WinSATUpdate
---

# IWinSATInitiateEvents::WinSATUpdate


## -description

<p class="CCE_Message">[IWinSATInitiateEvents::WinSATUpdate may be altered or unavailable for releases after Windows 8.1.]

Receives notification when an assessment is making progress.

## -parameters

### -param uCurrentTick [in]

The current progress tick of the assessment.

### -param uTickTotal [in]

The total number of progress ticks for the assessment.

### -param strCurrentState [in]

A string that contains the current state of the assessment. This string is valid during the life of this callback. Copy the string if you need it after the callback returns.

## -returns

This method should return  S_OK; the value is ignored.

## -remarks

You can use this method to determine the progress of a formal assessment.  

<div class="alert"><b>Note</b>  You can use the <i>uCurrentTick</i> and <i>uTickTotal</i> values to mark progress for formal assessments only; the values are zero for all other assessments.</div>
<div> </div>
You should keep your implementation short so you do not miss subsequent updates; you will not get new updates until the method returns.

<div class="alert"><b>Note</b>  If an instance of WinSAT is already running, it is possible that you could receive one or more update callbacks for the currently running assessment.</div>
<div> </div>

#### Examples

For an example implementation, see the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment">InitiateAssessment</a> or <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment">InitiateFormalAssessment</a> method of <a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents">IWinSATInitiateEvents</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iwinsatinitiateevents-winsatcomplete">IWinSATInitiateEvents::WinSATComplete</a>