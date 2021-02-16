---
UID: NF:reconcil.IReconcileInitiator.SetProgressFeedback
title: IReconcileInitiator::SetProgressFeedback (reconcil.h)
description: Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.
helpviewer_keywords: ["IReconcileInitiator interface [Legacy Windows Environment Features]","SetProgressFeedback method","IReconcileInitiator.SetProgressFeedback","IReconcileInitiator::SetProgressFeedback","SetProgressFeedback","SetProgressFeedback method [Legacy Windows Environment Features]","SetProgressFeedback method [Legacy Windows Environment Features]","IReconcileInitiator interface","_win32_IReconcileInitiator_SetProgressFeedback","lwef.ireconcileinitiator_setprogressfeedback","reconcil/IReconcileInitiator::SetProgressFeedback","shell.ireconcileinitiator_setprogressfeedback"]
old-location: lwef\ireconcileinitiator_setprogressfeedback.htm
tech.root: lwef
ms.assetid: faa685f1-e203-4d8a-a1c3-d544b8e5271d
ms.date: 12/05/2018
ms.keywords: IReconcileInitiator interface [Legacy Windows Environment Features],SetProgressFeedback method, IReconcileInitiator.SetProgressFeedback, IReconcileInitiator::SetProgressFeedback, SetProgressFeedback, SetProgressFeedback method [Legacy Windows Environment Features], SetProgressFeedback method [Legacy Windows Environment Features],IReconcileInitiator interface, _win32_IReconcileInitiator_SetProgressFeedback, lwef.ireconcileinitiator_setprogressfeedback, reconcil/IReconcileInitiator::SetProgressFeedback, shell.ireconcileinitiator_setprogressfeedback
req.header: reconcil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IReconcileInitiator::SetProgressFeedback
 - reconcil/IReconcileInitiator::SetProgressFeedback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IReconcileInitiator.SetProgressFeedback
---

# IReconcileInitiator::SetProgressFeedback


## -description

Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation. The amount is a fraction and is computed as the quotient of the <i>ulProgress</i> and <i>ulProgressMax</i> parameters. Reconcilers should call this method periodically during their reconciliation process.

## -parameters

### -param ulProgress

Type: <b>ULONG</b>

The numerator of the progress fraction.

### -param ulProgressMax

Type: <b>ULONG</b>

The denominator of the progress fraction.

## -returns

Type: <b>HRESULT</b>

Returns the S_OK value if successful, or the E_UNEXPECTED value if an unspecified error occurred.

## -remarks

The initiator typically uses this measure of progress to update a thermometer gauge or some other form of visual feedback for the user. The briefcase reconciler can change the value of <i>ulProgressMax</i> from call to call. This means successive calls to this method do not necessarily indicate steady forward progress. Backward progress is legal, although not desirable. It is the responsibility of the initiator to determine whether backward progress should be revealed to the user.

## -see-also

<a href="/windows/desktop/lwef/ireconcileinitiator">IReconcileInitiator</a>