---
UID: NF:strmif.IOverlayNotify.OnPaletteChange
title: IOverlayNotify::OnPaletteChange
author: windows-driver-content
description: The OnPaletteChange method provides notification that the palette of the window has changed.
old-location: dshow\ioverlaynotify_onpalettechange.htm
old-project: DirectShow
ms.assetid: 128e3834-d561-46d3-b32b-5bfd290f0995
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IOverlayNotify interface [DirectShow],OnPaletteChange method, IOverlayNotify.OnPaletteChange, IOverlayNotify::OnPaletteChange, IOverlayNotifyOnPaletteChange, OnPaletteChange, OnPaletteChange method [DirectShow], OnPaletteChange method [DirectShow],IOverlayNotify interface, dshow.ioverlaynotify_onpalettechange, strmif/IOverlayNotify::OnPaletteChange
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
-	IOverlayNotify.OnPaletteChange
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IOverlayNotify::OnPaletteChange


## -description



The <code>OnPaletteChange</code> method provides notification that the palette of the window has changed.




## -parameters




### -param dwColors [in]

Number of colors present.


### -param pPalette [in]

Pointer to the array of palette colors.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



Before returning, the filter should copy the array of <b>RGBQUAD</b> values, if necessary.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify Interface</a>
 

 

