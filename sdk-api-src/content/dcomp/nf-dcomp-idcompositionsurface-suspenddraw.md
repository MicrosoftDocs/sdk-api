---
UID: NF:dcomp.IDCompositionSurface.SuspendDraw
title: IDCompositionSurface::SuspendDraw (dcomp.h)

description: Suspends the drawing on this Microsoft DirectComposition surface object.
old-location: directcomp\idcompositionsurface_suspenddraw.htm
tech.root: directcomp
ms.assetid: B3CD2007-502C-48EF-989E-4C690B2B65D8

ms.date: 12/05/2018
ms.keywords: IDCompositionSurface interface [DirectComposition],SuspendDraw method, IDCompositionSurface.SuspendDraw, IDCompositionSurface::SuspendDraw, SuspendDraw, SuspendDraw method [DirectComposition], SuspendDraw method [DirectComposition],IDCompositionSurface interface, dcomp/IDCompositionSurface::SuspendDraw, directcomp.idcompositionsurface_suspenddraw
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionSurface.SuspendDraw"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurface.SuspendDraw
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionSurface::SuspendDraw


## -description


Suspends the drawing on this Microsoft DirectComposition surface object.


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code, which can include <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED</a> and <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED</a>. 




## -remarks



Because only one surface can be open for drawing at a time, calling <b>SuspendDraw</b> allows the user to call <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> on a different surface. Drawing to this surface can be resumed by calling <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw">IDCompositionSurface::ResumeDraw</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw">IDCompositionSurface::ResumeDraw</a>
 

 

