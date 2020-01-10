---
UID: NF:tsvirtualchannels.IWTSBitmapRenderer.GetRendererStatistics
title: IWTSBitmapRenderer::GetRendererStatistics (tsvirtualchannels.h)
description: Retrieves statistics for the RemoteFX media redirection bitmap renderer.
old-location: termserv\iwtsbitmaprenderer_getrendererstatistics.htm
tech.root: TermServ
ms.assetid: 9BC4C091-053E-4E94-BF65-91AEB03C355F
ms.date: 12/05/2018
ms.keywords: GetRendererStatistics, GetRendererStatistics method [Remote Desktop Services], GetRendererStatistics method [Remote Desktop Services],IWTSBitmapRenderer interface, IWTSBitmapRenderer interface [Remote Desktop Services],GetRendererStatistics method, IWTSBitmapRenderer.GetRendererStatistics, IWTSBitmapRenderer::GetRendererStatistics, termserv.iwtsbitmaprenderer_getrendererstatistics, tsvirtualchannels/IWTSBitmapRenderer::GetRendererStatistics
f1_keywords:
- tsvirtualchannels/IWTSBitmapRenderer.GetRendererStatistics
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tsvirtualchannels.h
api_name:
- IWTSBitmapRenderer.GetRendererStatistics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSBitmapRenderer::GetRendererStatistics


## -description


Retrieves statistics for the RemoteFX media redirection bitmap renderer.


## -parameters




### -param pStatistics [out]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/tsvirtualchannels/ns-tsvirtualchannels-bitmap_renderer_statistics">BITMAP_RENDERER_STATISTICS</a>*</b>

The address of a 
      <a href="https://docs.microsoft.com/windows/win32/api/tsvirtualchannels/ns-tsvirtualchannels-bitmap_renderer_statistics">BITMAP_RENDERER_STATISTICS</a> structure 
      that receives the bitmap rendering statistics.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/tsvirtualchannels/ns-tsvirtualchannels-bitmap_renderer_statistics">BITMAP_RENDERER_STATISTICS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderer">IWTSBitmapRenderer</a>
 

 

