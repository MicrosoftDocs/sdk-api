---
UID: NF:amvideo.IFullScreenVideoEx.SetDefault
title: IFullScreenVideoEx::SetDefault
author: windows-sdk-content
description: The SetDefault method saves the current settings.
old-location: dshow\ifullscreenvideoex_setdefault.htm
tech.root: DirectShow
ms.assetid: 1821703c-0da1-4b3e-a921-a66770b8ee0d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetDefault method, IFullScreenVideoEx.SetDefault, IFullScreenVideoEx::SetDefault, IFullScreenVideoSetDefault, SetDefault, SetDefault method [DirectShow], SetDefault method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetDefault, dshow.ifullscreenvideoex_setdefault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amvideo.h
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
 - IFullScreenVideoEx.SetDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFullScreenVideoEx::SetDefault


## -description



The <code>SetDefault</code> method saves the current settings.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Normally, the properties set through this interface apply only to the current instance of the Full Screen Renderer. Calling this method saves the current values as the global default. This method persists the following information:

<ul>
<li>The clip factor.</li>
<li>The enabled flag for each display mode.</li>
</ul>
It does not persist the caption or the hide-when-deactivated flag.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390056(v=VS.85).aspx">IFullScreenVideoEx Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390065(v=VS.85).aspx">IFullScreenVideoEx::HideOnDeactivate</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390072(v=VS.85).aspx">IFullScreenVideoEx::SetCaption</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390073(v=VS.85).aspx">IFullScreenVideoEx::SetClipFactor</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390075(v=VS.85).aspx">IFullScreenVideoEx::SetEnabled</a>
 

 

