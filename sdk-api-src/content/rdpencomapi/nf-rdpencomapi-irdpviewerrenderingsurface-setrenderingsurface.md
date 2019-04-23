---
UID: NF:rdpencomapi.IRDPViewerRenderingSurface.SetRenderingSurface
title: IRDPViewerRenderingSurface::SetRenderingSurface (rdpencomapi.h)
author: windows-sdk-content
description: Sets the rendering surface to be used by the viewer.
old-location: rdp\irdpviewerrenderingsurface_setrenderingsurface.htm
tech.root: rdp
ms.assetid: e70541ab-fc23-4960-be38-8eb6849ab14f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRDPViewerRenderingSurface interface [RDP],SetRenderingSurface method, IRDPViewerRenderingSurface.SetRenderingSurface, IRDPViewerRenderingSurface::SetRenderingSurface, SetRenderingSurface, SetRenderingSurface method [RDP], SetRenderingSurface method [RDP],IRDPViewerRenderingSurface interface, rdp.irdpviewerrenderingsurface_setrenderingsurface, rdpencomapi/IRDPViewerRenderingSurface::SetRenderingSurface
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPViewerRenderingSurface.SetRenderingSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPViewerRenderingSurface::SetRenderingSurface


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/24d818ec-f58d-4bf1-adf8-c15560595147">IRDPViewerRenderingSurface</a> interface is no longer available for use as of Windows 10, version 1709.]

Sets the rendering surface to be used by the viewer.


## -parameters




### -param pRenderingSurface [in]

The address of the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> object to use for the rendering surface.


### -param surfaceWidth [in]

The width, in pixels, of the rendering surface.


### -param surfaceHeight [in]

The height, in pixels, of the rendering surface.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/24d818ec-f58d-4bf1-adf8-c15560595147">IRDPViewerRenderingSurface</a>
 

 

