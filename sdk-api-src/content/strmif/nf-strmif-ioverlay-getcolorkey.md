---
UID: NF:strmif.IOverlay.GetColorKey
title: IOverlay::GetColorKey
author: windows-sdk-content
description: The GetColorKey method retrieves the current color key used for chroma keying.
old-location: dshow\ioverlay_getcolorkey.htm
tech.root: DirectShow
ms.assetid: fc9e414e-be53-46e7-b329-23f17fc23725
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetColorKey, GetColorKey method [DirectShow], GetColorKey method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetColorKey method, IOverlay.GetColorKey, IOverlay::GetColorKey, IOverlayGetColorKey, dshow.ioverlay_getcolorkey, strmif/IOverlay::GetColorKey
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IOverlay.GetColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOverlay::GetColorKey


## -description



The <code>GetColorKey</code> method retrieves the current color key used for chroma keying.




## -parameters




### -param pColorKey [out]

Pointer to a variable that receives the current color key for chroma keying.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



If you change the color key by using the <a href="https://msdn.microsoft.com/dacbaf03-348f-403d-9c2c-aed8ec344879">IOverlay::SetColorKey</a> method, all the advise links receive an <a href="https://msdn.microsoft.com/a1e7fc88-a50a-4832-9b29-21b94184f1c7">IOverlayNotify::OnColorKeyChange</a> callback method with the new color.

If no color key is currently being used, this method returns VFW_E_NO_COLOR_KEY_SET.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 

