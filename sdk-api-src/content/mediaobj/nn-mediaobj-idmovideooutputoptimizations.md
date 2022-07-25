---
UID: NN:mediaobj.IDMOVideoOutputOptimizations
title: IDMOVideoOutputOptimizations (mediaobj.h)
description: The IDMOVideoOutputOptimizations interface supports video optimizations on a Microsoft DirectX Media Object (DMO).
helpviewer_keywords: ["IDMOVideoOutputOptimizations","IDMOVideoOutputOptimizations interface [DirectShow]","IDMOVideoOutputOptimizations interface [DirectShow]","described","IDMOVideoOutputOptimizationsInterface","dshow.idmovideooutputoptimizations","mediaobj/IDMOVideoOutputOptimizations"]
old-location: dshow\idmovideooutputoptimizations.htm
tech.root: dshow
ms.assetid: 1e87d0e1-68be-4f86-aae2-cff3edfa573b
ms.date: 12/05/2018
ms.keywords: IDMOVideoOutputOptimizations, IDMOVideoOutputOptimizations interface [DirectShow], IDMOVideoOutputOptimizations interface [DirectShow],described, IDMOVideoOutputOptimizationsInterface, dshow.idmovideooutputoptimizations, mediaobj/IDMOVideoOutputOptimizations
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMOVideoOutputOptimizations
 - mediaobj/IDMOVideoOutputOptimizations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOVideoOutputOptimizations
---

# IDMOVideoOutputOptimizations interface


## -description

The <code>IDMOVideoOutputOptimizations</code> interface supports video optimizations on a Microsoft DirectX Media Object (DMO).

## -inheritance

The <b>IDMOVideoOutputOptimizations</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDMOVideoOutputOptimizations</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

This interface enables an application to negotiate with a DMO about video output optimizations. A DMO exposes this interface when it can perform optimizations that require support from the application. The application can query the DMO for its preferred features, and then agree (or not agree) to provide them. The DMO must process output even if the application rejects the optimizations.

For example, a video decoder might generate an output frame by applying deltas to the previous output frame. When queried, it requests that the application supply the previous frame in the output buffer. The application can agree to this request or not.

Video optimizations are negotiated separately for each output stream.

The following pseudo-code shows how an application might negotiate with the DMO:


```
IDMOVideoOutputOptimizations *pVidOpt;
// Query the DMO for IDMOVideoOutputOptimizations (not shown).

BOOL  bWantsPreviousBuffer = FALSE;
DWORD wFlags;
pVidOpt->QueryOperationModePreferences(0,&dwFlags);

if (dwFlags & DMO_VOSF_NEEDS_PREVIOUS_SAMPLE) 
{
    // Agree to the request.      
    pVidOpt->SetOperationMode(0, DMO_VOSF_NEEDS_PREVIOUS_SAMPLE);
    bWantsPreviousBuffer = TRUE;
}

// Processing loop
while (there is input).
{
    ProcessInput(0, ...);
    if (bWantsPreviousBuffer)
        pDMO->ProcessOutput(0, ...) // Use the same buffer as last time.
    else
        pDMO->ProcessOutput(0, ...) // OK to use a new buffer.
}
```
