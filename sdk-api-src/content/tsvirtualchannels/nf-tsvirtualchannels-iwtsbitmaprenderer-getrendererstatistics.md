---
UID: NF:tsvirtualchannels.IWTSBitmapRenderer.GetRendererStatistics
title: IWTSBitmapRenderer::GetRendererStatistics
author: windows-driver-content
description: Retrieves statistics for the RemoteFX media redirection bitmap renderer.
old-location: termserv\iwtsbitmaprenderer_getrendererstatistics.htm
old-project: TermServ
ms.assetid: 9BC4C091-053E-4E94-BF65-91AEB03C355F
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetRendererStatistics, GetRendererStatistics method [Remote Desktop Services], GetRendererStatistics method [Remote Desktop Services],IWTSBitmapRenderer interface, IWTSBitmapRenderer interface [Remote Desktop Services],GetRendererStatistics method, IWTSBitmapRenderer.GetRendererStatistics, IWTSBitmapRenderer::GetRendererStatistics, termserv.iwtsbitmaprenderer_getrendererstatistics, tsvirtualchannels/IWTSBitmapRenderer::GetRendererStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSVirtualChannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTSSBX_SESSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tsvirtualchannels.h
api_name:
-	IWTSBitmapRenderer.GetRendererStatistics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSBitmapRenderer::GetRendererStatistics


## -description


Retrieves statistics for the RemoteFX media redirection bitmap renderer.


## -parameters




### -param pStatistics [out]

Type: <b><a href="https://msdn.microsoft.com/111FA0B3-BFC1-4BD7-8BF0-C0C746A39C5D">BITMAP_RENDERER_STATISTICS</a>*</b>

The address of a 
      <a href="https://msdn.microsoft.com/111FA0B3-BFC1-4BD7-8BF0-C0C746A39C5D">BITMAP_RENDERER_STATISTICS</a> structure 
      that receives the bitmap rendering statistics.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/111FA0B3-BFC1-4BD7-8BF0-C0C746A39C5D">BITMAP_RENDERER_STATISTICS</a>



<a href="https://msdn.microsoft.com/6930683e-bb9e-499c-b44f-27938faff3db">IWTSBitmapRenderer</a>
 

 

