---
UID: NF:dcomp.IDCompositionSurface.EndDraw
title: IDCompositionSurface::EndDraw
author: windows-sdk-content
description: Marks the end of drawing on this Microsoft DirectComposition surface object.
old-location: directcomp\idcompositionsurface_enddraw.htm
tech.root: directcomp
ms.assetid: 127195F7-6000-4D8C-B850-3E4D40BC4082
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: EndDraw, EndDraw method [DirectComposition], EndDraw method [DirectComposition],IDCompositionSurface interface, IDCompositionSurface interface [DirectComposition],EndDraw method, IDCompositionSurface.EndDraw, IDCompositionSurface::EndDraw, dcomp/IDCompositionSurface::EndDraw, directcomp.idcompositionsurface_enddraw
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
 - IDCompositionSurface.EndDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSurface::EndDraw


## -description


Marks the end of drawing on this Microsoft DirectComposition surface object.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code, which can include <a href="directcomposition_error_codes.htm">DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED</a>. 




## -remarks



This method completes an update that was begun by a previous call to the <a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">IDCompositionSurface::BeginDraw</a> method. After this method returns, the application can start another update on the same surface object or on a different one.



If the application calls <a href="https://msdn.microsoft.com/8C24DE03-CF1E-4DC4-8C27-913DAD278579">IDCompositionDevice2::Commit</a> before calling <b>IDCompositionSurface::EndDraw</b> for a surface with a pending update, that update is not processed by that Commit call. The update only takes effect on screen after the application calls <b>IDCompositionSurface::EndDraw</b> followed by the IDCompositionDevice2::Commit method.




## -see-also




<a href="https://msdn.microsoft.com/E271B4DC-5F09-426A-A5D3-43A48F30CB24">IDCompositionSurface</a>



<a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">IDCompositionSurface::BeginDraw</a>



<a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">IDCompositionSurface::EndDraw</a>
 

 

