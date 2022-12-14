---
UID: NF:dcomp.IDCompositionSurface.ResumeDraw
title: IDCompositionSurface::ResumeDraw (dcomp.h)
description: Resumes drawing on this Microsoft DirectComposition surface object.
helpviewer_keywords: ["IDCompositionSurface interface [DirectComposition]","ResumeDraw method","IDCompositionSurface.ResumeDraw","IDCompositionSurface::ResumeDraw","ResumeDraw","ResumeDraw method [DirectComposition]","ResumeDraw method [DirectComposition]","IDCompositionSurface interface","dcomp/IDCompositionSurface::ResumeDraw","directcomp.idcompositionsurface_resumedraw"]
old-location: directcomp\idcompositionsurface_resumedraw.htm
tech.root: directcomp
ms.assetid: EE008AAB-0C79-4D60-953C-7A9BCFED2C41
ms.date: 12/05/2018
ms.keywords: IDCompositionSurface interface [DirectComposition],ResumeDraw method, IDCompositionSurface.ResumeDraw, IDCompositionSurface::ResumeDraw, ResumeDraw, ResumeDraw method [DirectComposition], ResumeDraw method [DirectComposition],IDCompositionSurface interface, dcomp/IDCompositionSurface::ResumeDraw, directcomp.idcompositionsurface_resumedraw
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionSurface::ResumeDraw
 - dcomp/IDCompositionSurface::ResumeDraw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurface.ResumeDraw
---

# IDCompositionSurface::ResumeDraw


## -description

Resumes drawing on this Microsoft DirectComposition surface object.



## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code, which can include <a href="/windows/desktop/directcomp/directcomposition-error-codes">DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED</a> and <a href="/windows/desktop/directcomp/directcomposition-error-codes">DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED</a>.

## -remarks

 This method allows the surface update to continue unless there are other surfaces that have active, unsuspended draws.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw">IDCompositionSurface::SuspendDraw</a>
