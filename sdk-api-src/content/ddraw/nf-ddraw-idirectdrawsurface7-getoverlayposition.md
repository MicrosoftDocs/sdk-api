---
UID: NF:ddraw.IDirectDrawSurface7.GetOverlayPosition
title: IDirectDrawSurface7::GetOverlayPosition (ddraw.h)
description: Retrieves the display coordinates of this surface. This method is used on a visible, active overlay surface (that is, a surface that has the DDSCAPS_OVERLAY flag set).
helpviewer_keywords: ["GetOverlayPosition","GetOverlayPosition method [DirectDraw]","GetOverlayPosition method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetOverlayPosition method","IDirectDrawSurface7.GetOverlayPosition","IDirectDrawSurface7::GetOverlayPosition","ddraw/IDirectDrawSurface7::GetOverlayPosition","directdraw.idirectdrawsurface7_getoverlayposition"]
old-location: directdraw\idirectdrawsurface7_getoverlayposition.htm
tech.root: directdraw
ms.assetid: 008502f7-468f-4d79-a309-75ebdbe29ff3
ms.date: 12/05/2018
ms.keywords: GetOverlayPosition, GetOverlayPosition method [DirectDraw], GetOverlayPosition method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetOverlayPosition method, IDirectDrawSurface7.GetOverlayPosition, IDirectDrawSurface7::GetOverlayPosition, ddraw/IDirectDrawSurface7::GetOverlayPosition, directdraw.idirectdrawsurface7_getoverlayposition
f1_keywords:
- ddraw/IDirectDrawSurface7.GetOverlayPosition
dev_langs:
- c++
req.header: ddraw.h
req.include-header: 
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDrawSurface7.GetOverlayPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawSurface7::GetOverlayPosition


## -description


Retrieves the display coordinates of this surface. This method is used on a visible, active overlay surface (that is, a surface that has the DDSCAPS_OVERLAY flag set).


## -parameters




### -param arg1 [out]

A pointer to a variable that receives the x- display coordinate of this surface if the call succeeds.


### -param arg2 [out]

A pointer to a variable that receives the y-display coordinate of this surface if the call succeeds.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDPOSITION</li>
<li>DDERR_NOOVERLAYDEST</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
<li>DDERR_OVERLAYNOTVISIBLE</li>
<li>DDERR_SURFACELOST</li>
</ul>



## -remarks



You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the  <b>GetOverlayPosition</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 

