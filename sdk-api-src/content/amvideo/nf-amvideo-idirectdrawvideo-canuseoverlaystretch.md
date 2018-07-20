---
UID: NF:amvideo.IDirectDrawVideo.CanUseOverlayStretch
title: IDirectDrawVideo::CanUseOverlayStretch
author: windows-sdk-content
description: The CanUseOverlayStretch method determines whether the renderer will check overlay restrictions.
old-location: dshow\idirectdrawvideo_canuseoverlaystretch.htm
old-project: DirectShow
ms.assetid: 35af80c9-7cc7-46c7-899c-c47f56a4ec17
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CanUseOverlayStretch, CanUseOverlayStretch method [DirectShow], CanUseOverlayStretch method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],CanUseOverlayStretch method, IDirectDrawVideo.CanUseOverlayStretch, IDirectDrawVideo::CanUseOverlayStretch, IDirectDrawVideoCanUseOverlayStretch, amvideo/IDirectDrawVideo::CanUseOverlayStretch, dshow.idirectdrawvideo_canuseoverlaystretch
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDirectDrawVideo.CanUseOverlayStretch
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawVideo::CanUseOverlayStretch


## -description



The <code>CanUseOverlayStretch</code> method determines whether the renderer will check overlay restrictions.




## -parameters




### -param UseOverlayStretch

Pointer to a value indicating whether the renderer can use overlay restrictions. OATRUE indicates the renderer will check overlay restrictions; OAFALSE indicates it will not.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



For a description of overlay stretching, see <a href="https://msdn.microsoft.com/e617b40d-ba5b-4fc8-825e-3c751f72bc2c">IDirectDrawVideo::UseOverlayStretch</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

