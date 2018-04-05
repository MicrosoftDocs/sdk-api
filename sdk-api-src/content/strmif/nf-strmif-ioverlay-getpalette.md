---
UID: NF:strmif.IOverlay.GetPalette
title: IOverlay::GetPalette method
author: windows-driver-content
description: The GetPalette method retrieves the current system palette.
old-location: dshow\ioverlay_getpalette.htm
old-project: DirectShow
ms.assetid: 993c80fb-fa67-4dd6-815b-8e15d2f7f495
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetPalette method [DirectShow], GetPalette method [DirectShow], IOverlay interface, GetPalette,IOverlay.GetPalette, IOverlay, IOverlay interface [DirectShow], GetPalette method, IOverlay::GetPalette, IOverlayGetPalette, dshow.ioverlay_getpalette, strmif/IOverlay::GetPalette
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IOverlay.GetPalette
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IOverlay::GetPalette method


## -description



The <code>GetPalette</code> method retrieves the current system palette.




## -parameters




### -param pdwColors [out]

Pointer to a variable that receives the number of colors present.


### -param ppPalette [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structure describing the palette.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 

