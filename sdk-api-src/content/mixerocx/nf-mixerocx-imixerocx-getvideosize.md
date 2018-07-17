---
UID: NF:mixerocx.IMixerOCX.GetVideoSize
title: IMixerOCX::GetVideoSize
author: windows-sdk-content
description: The GetVideoSize method retrieves the current size of the video rectangle.
old-location: dshow\imixerocx_getvideosize.htm
old-project: DirectShow
ms.assetid: e4cc71b6-23a5-4610-ac59-06484af6d0b4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetVideoSize, GetVideoSize method [DirectShow], GetVideoSize method [DirectShow],IMixerOCX interface, IMixerOCX interface [DirectShow],GetVideoSize method, IMixerOCX.GetVideoSize, IMixerOCX::GetVideoSize, IMixerOCXGetVideoSize, dshow.imixerocx_getvideosize, mixerocx/IMixerOCX::GetVideoSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mixerocx.h
req.include-header: 
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
req.typenames: WIN32_FIND_DATAW, *PWIN32_FIND_DATAW, *LPWIN32_FIND_DATAW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerOCX.GetVideoSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerOCX::GetVideoSize


## -description



The <code>GetVideoSize</code> method retrieves the current size of the video rectangle.




## -parameters




### -param pdwVideoWidth [out]

Pointer that receives the video width in pixels.


### -param pdwVideoHeight [out]

Pointer that receives the video height in pixels.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/b80d720d-921d-4d24-a168-49944cfcc411">IMixerOCX Interface</a>



<a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>
 

 

