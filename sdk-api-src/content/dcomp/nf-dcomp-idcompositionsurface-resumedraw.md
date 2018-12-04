---
UID: NF:dcomp.IDCompositionSurface.ResumeDraw
title: IDCompositionSurface::ResumeDraw
author: windows-sdk-content
description: Resumes drawing on this Microsoft DirectComposition surface object.
old-location: directcomp\idcompositionsurface_resumedraw.htm
tech.root: directcomp
ms.assetid: EE008AAB-0C79-4D60-953C-7A9BCFED2C41
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDCompositionSurface interface [DirectComposition],ResumeDraw method, IDCompositionSurface.ResumeDraw, IDCompositionSurface::ResumeDraw, ResumeDraw, ResumeDraw method [DirectComposition], ResumeDraw method [DirectComposition],IDCompositionSurface interface, dcomp/IDCompositionSurface::ResumeDraw, directcomp.idcompositionsurface_resumedraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDCompositionSurface.ResumeDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSurface::ResumeDraw


## -description


Resumes drawing on this Microsoft DirectComposition surface object.


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code, which can include <a href="directcomposition_error_codes.htm">DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED</a> and <a href="directcomposition_error_codes.htm">DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED</a>. 




## -remarks



 This method allows the surface update to continue unless there are other surfaces that have active, unsuspended draws.




## -see-also




<a href="https://msdn.microsoft.com/E271B4DC-5F09-426A-A5D3-43A48F30CB24">IDCompositionSurface</a>



<a href="https://msdn.microsoft.com/B3CD2007-502C-48EF-989E-4C690B2B65D8">IDCompositionSurface::SuspendDraw</a>
 

 

