---
UID: NF:comsvcs.IThreadPoolKnobs.SetDeleteDelay
title: IThreadPoolKnobs::SetDeleteDelay (comsvcs.h)
description: Sets the number of milliseconds a pooled thread can idle before being destroyed.
helpviewer_keywords: ["IThreadPoolKnobs interface [COM+]","SetDeleteDelay method","IThreadPoolKnobs.SetDeleteDelay","IThreadPoolKnobs::SetDeleteDelay","SetDeleteDelay","SetDeleteDelay method [COM+]","SetDeleteDelay method [COM+]","IThreadPoolKnobs interface","_cos_IThreadPoolKnobs_SetDeleteDelay","comsvcs/IThreadPoolKnobs::SetDeleteDelay","cos.ithreadpoolknobs_setdeletedelay"]
old-location: cos\ithreadpoolknobs_setdeletedelay.htm
tech.root: cos
ms.assetid: dd01dc40-fbf6-48f9-bef7-8a935a6adf28
ms.date: 12/05/2018
ms.keywords: IThreadPoolKnobs interface [COM+],SetDeleteDelay method, IThreadPoolKnobs.SetDeleteDelay, IThreadPoolKnobs::SetDeleteDelay, SetDeleteDelay, SetDeleteDelay method [COM+], SetDeleteDelay method [COM+],IThreadPoolKnobs interface, _cos_IThreadPoolKnobs_SetDeleteDelay, comsvcs/IThreadPoolKnobs::SetDeleteDelay, cos.ithreadpoolknobs_setdeletedelay
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IThreadPoolKnobs::SetDeleteDelay
 - comsvcs/IThreadPoolKnobs::SetDeleteDelay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IThreadPoolKnobs.SetDeleteDelay
---

# IThreadPoolKnobs::SetDeleteDelay


## -description

Sets the number of milliseconds a pooled thread can idle before being destroyed.

## -parameters

### -param msecDeleteDelay [in]

The number of milliseconds a pooled thread can idle before being destroyed. A zero value indicates that threads are never automatically deleted.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>