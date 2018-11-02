---
UID: NF:dcomp.IDCompositionVirtualSurface.Trim
title: IDCompositionVirtualSurface::Trim
author: windows-sdk-content
description: Discards pixels that fall outside of the specified trim rectangles.
old-location: directcomp\idcompositionvirtualsurface_trim.htm
tech.root: directcomp
ms.assetid: 5A4F516F-B031-47E6-9A3D-068CF2C3D53A
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionVirtualSurface interface [DirectComposition],Trim method, IDCompositionVirtualSurface.Trim, IDCompositionVirtualSurface::Trim, Trim, Trim method [DirectComposition], Trim method [DirectComposition],IDCompositionVirtualSurface interface, dcomp/IDCompositionVirtualSurface::Trim, directcomp.idcompositionvirtualsurface_trim
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
 - IDCompositionVirtualSurface.Trim
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVirtualSurface::Trim


## -description


Discards pixels that fall outside of the specified trim rectangles.


## -parameters




### -param rectangles [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

An array of rectangles to keep.


### -param count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of rectangles in the <i>rectangles</i> array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A virtual surface might not  have enough storage for every pixel in the surface. An application instructs the composition engine to allocate memory for the surface by calling the <a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">IDCompositionSurface::BeginDraw</a> method, and to release memory for the surface by calling the <b>IDCompositionVirtualSurface::Trim</b> method. The array of rectangles represents the regions of the virtual surface that should remain allocated after this method returns. Any pixels that are outside the specified set of rectangles are no longer used for texturing, and their memory may be reclaimed.



If the <i>count</i> parameter is zero, no pixels are kept, and all of the memory allocated for the virtual surface may be reclaimed. The <i>rectangles</i> parameter can be NULL only if the <i>count</i> parameter is zero.

This method fails if <a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">IDCompositionSurface::BeginDraw</a> was called for this bitmap without a corresponding call to <a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">IDCompositionSurface::EndDraw</a>.




## -see-also




<a href="https://msdn.microsoft.com/85619C69-F5AE-4F07-AE56-7305BBECD58F">IDCompositionDevice::CreateVirtualSurface</a>



<a href="https://msdn.microsoft.com/51E8D52C-2446-46B6-A5C1-0DC7FA9DF4CC">IDCompositionVirtualSurface </a>



<a href="https://msdn.microsoft.com/BB86CDA8-1DF0-436D-9FA3-95293E2B8C0E">IDCompositionVirtualSurface::Resize</a>
 

 

