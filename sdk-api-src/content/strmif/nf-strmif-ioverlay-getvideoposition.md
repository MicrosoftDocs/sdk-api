---
UID: NF:strmif.IOverlay.GetVideoPosition
title: IOverlay::GetVideoPosition
author: windows-sdk-content
description: The GetVideoPosition method retrieves the current video source and destination rectangles.
old-location: dshow\ioverlay_getvideoposition.htm
old-project: DirectShow
ms.assetid: a140cc63-29a1-4c81-8393-7f4342c7b7cc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetVideoPosition, GetVideoPosition method [DirectShow], GetVideoPosition method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetVideoPosition method, IOverlay.GetVideoPosition, IOverlay::GetVideoPosition, IOverlayGetVideoPosition, dshow.ioverlay_getvideoposition, strmif/IOverlay::GetVideoPosition
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IOverlay.GetVideoPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IOverlay::GetVideoPosition


## -description



The <code>GetVideoPosition</code> method retrieves the current video source and destination rectangles.




## -parameters




### -param pSourceRect [out]

Pointer to a <b>RECT</b> structure that receives the source rectangle.


### -param pDestinationRect [in]

Pointer to to a <b>RECT</b> structure that receives the destination rectangle.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 

