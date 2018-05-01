---
UID: NF:amvideo.IDirectDrawVideo.GetSurfaceDesc
title: IDirectDrawVideo::GetSurfaceDesc method
author: windows-driver-content
description: The GetSurfaceDesc method retrieves a DDSURFACEDESC structure describing the current DirectDraw surface.
old-location: dshow\idirectdrawvideo_getsurfacedesc.htm
old-project: DirectShow
ms.assetid: f3884dbf-c75c-45f7-953c-bfdc14734820
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetSurfaceDesc method [DirectShow], GetSurfaceDesc method [DirectShow], IDirectDrawVideo interface, GetSurfaceDesc,IDirectDrawVideo.GetSurfaceDesc, IDirectDrawVideo, IDirectDrawVideo interface [DirectShow], GetSurfaceDesc method, IDirectDrawVideo::GetSurfaceDesc, IDirectDrawVideoGetSurfaceDesc, amvideo/IDirectDrawVideo::GetSurfaceDesc, dshow.idirectdrawvideo_getsurfacedesc
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDirectDrawVideo.GetSurfaceDesc
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawVideo::GetSurfaceDesc method


## -description



The <code>GetSurfaceDesc</code> method retrieves a <b>DDSURFACEDESC</b> structure describing the current DirectDraw surface.




## -parameters




### -param pSurfaceDesc

Pointer to a <b>DDSURFACEDESC</b> structure describing the current DirectDraw surface.


## -returns



Returns an <b>HRESULT</b> value. If no surface has been allocated, this method will return E_FAIL. If a DCI primary surface is in use, the <b>DDSURFACEDESC</b> structure will not be filled in and the call will return S_FALSE.




## -remarks



Surfaces are allocated only when the renderer is paused. After the renderer has been paused, it cannot release the surfaces when stopped.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

