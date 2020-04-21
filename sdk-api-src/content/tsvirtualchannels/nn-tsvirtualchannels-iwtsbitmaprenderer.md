---
UID: NN:tsvirtualchannels.IWTSBitmapRenderer
title: IWTSBitmapRenderer (tsvirtualchannels.h)
description: Used by a dynamic virtual channel plug-in to render bitmaps.helpviewer_keywords: ["IWTSBitmapRenderer","IWTSBitmapRenderer interface [Remote Desktop Services]","IWTSBitmapRenderer interface [Remote Desktop Services]","described","termserv.iwtsbitmaprenderer","tsvirtualchannels/IWTSBitmapRenderer"]
old-location: termserv\iwtsbitmaprenderer.htm
tech.root: TermServ
ms.assetid: 6930683e-bb9e-499c-b44f-27938faff3db
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRenderer, IWTSBitmapRenderer interface [Remote Desktop Services], IWTSBitmapRenderer interface [Remote Desktop Services],described, termserv.iwtsbitmaprenderer, tsvirtualchannels/IWTSBitmapRenderer
f1_keywords:
- tsvirtualchannels/IWTSBitmapRenderer
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
- IWTSBitmapRenderer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSBitmapRenderer interface


## -description


Used by a dynamic virtual channel plug-in to render bitmaps. This interface is implemented by the rendering service. The plug-in obtains a pointer to this interface by using the <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderservice-getmappedrenderer">IWTSBitmapRenderService::GetMappedRenderer</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSBitmapRenderer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSBitmapRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSBitmapRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderer-getrendererstatistics">GetRendererStatistics</a>
</td>
<td align="left" width="63%">
Retrieves statistics for the RemoteFX media redirection bitmap renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderer-removemapping">RemoveMapping</a>
</td>
<td align="left" width="63%">
Called by a dynamic virtual channel plug-in to remove a render mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderer-render">Render</a>
</td>
<td align="left" width="63%">
Called by a dynamic virtual channel plug-in to render bitmaps.

</td>
</tr>
</table> 

