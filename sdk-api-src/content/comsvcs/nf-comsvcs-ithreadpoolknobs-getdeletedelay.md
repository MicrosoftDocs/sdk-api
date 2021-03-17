---
UID: NF:comsvcs.IThreadPoolKnobs.GetDeleteDelay
title: IThreadPoolKnobs::GetDeleteDelay (comsvcs.h)
description: Retrieves the number of milliseconds a pooled thread can idle before being destroyed.
helpviewer_keywords: ["GetDeleteDelay","GetDeleteDelay method [COM+]","GetDeleteDelay method [COM+]","IThreadPoolKnobs interface","IThreadPoolKnobs interface [COM+]","GetDeleteDelay method","IThreadPoolKnobs.GetDeleteDelay","IThreadPoolKnobs::GetDeleteDelay","_cos_IThreadPoolKnobs_GetDeleteDelay","comsvcs/IThreadPoolKnobs::GetDeleteDelay","cos.ithreadpoolknobs_getdeletedelay"]
old-location: cos\ithreadpoolknobs_getdeletedelay.htm
tech.root: cos
ms.assetid: 93404c39-b4f8-4247-a437-fd373b0b68fe
ms.date: 12/05/2018
ms.keywords: GetDeleteDelay, GetDeleteDelay method [COM+], GetDeleteDelay method [COM+],IThreadPoolKnobs interface, IThreadPoolKnobs interface [COM+],GetDeleteDelay method, IThreadPoolKnobs.GetDeleteDelay, IThreadPoolKnobs::GetDeleteDelay, _cos_IThreadPoolKnobs_GetDeleteDelay, comsvcs/IThreadPoolKnobs::GetDeleteDelay, cos.ithreadpoolknobs_getdeletedelay
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
 - IThreadPoolKnobs::GetDeleteDelay
 - comsvcs/IThreadPoolKnobs::GetDeleteDelay
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
 - IThreadPoolKnobs.GetDeleteDelay
---

# IThreadPoolKnobs::GetDeleteDelay


## -description

Retrieves the number of milliseconds a pooled thread can idle before being destroyed.

## -parameters

### -param pmsecDeleteDelay [out]

The number of milliseconds a pooled thread can idle before being destroyed. A zero value indicates that threads are never automatically deleted.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>