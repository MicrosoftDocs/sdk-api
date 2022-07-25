---
UID: NF:dcomp.IDCompositionSurface.EndDraw
title: IDCompositionSurface::EndDraw (dcomp.h)
description: Marks the end of drawing on this Microsoft DirectComposition surface object.
helpviewer_keywords: ["EndDraw","EndDraw method [DirectComposition]","EndDraw method [DirectComposition]","IDCompositionSurface interface","IDCompositionSurface interface [DirectComposition]","EndDraw method","IDCompositionSurface.EndDraw","IDCompositionSurface::EndDraw","dcomp/IDCompositionSurface::EndDraw","directcomp.idcompositionsurface_enddraw"]
old-location: directcomp\idcompositionsurface_enddraw.htm
tech.root: directcomp
ms.assetid: 127195F7-6000-4D8C-B850-3E4D40BC4082
ms.date: 12/05/2018
ms.keywords: EndDraw, EndDraw method [DirectComposition], EndDraw method [DirectComposition],IDCompositionSurface interface, IDCompositionSurface interface [DirectComposition],EndDraw method, IDCompositionSurface.EndDraw, IDCompositionSurface::EndDraw, dcomp/IDCompositionSurface::EndDraw, directcomp.idcompositionsurface_enddraw
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
 - IDCompositionSurface::EndDraw
 - dcomp/IDCompositionSurface::EndDraw
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
 - IDCompositionSurface.EndDraw
---

# IDCompositionSurface::EndDraw


## -description

Marks the end of drawing on this Microsoft DirectComposition surface object.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code, which can include <a href="/windows/desktop/directcomp/directcomposition-error-codes">DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED</a>.

## -remarks

This method completes an update that was begun by a previous call to the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> method. After this method returns, the application can start another update on the same surface object or on a different one.



If the application calls <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-commit">IDCompositionDevice2::Commit</a> before calling <b>IDCompositionSurface::EndDraw</b> for a surface with a pending update, that update is not processed by that Commit call. The update only takes effect on screen after the application calls <b>IDCompositionSurface::EndDraw</b> followed by the IDCompositionDevice2::Commit method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-enddraw">IDCompositionSurface::EndDraw</a>
