---
UID: NN:tsvirtualchannels.IWTSBitmapRenderService
title: IWTSBitmapRenderService (tsvirtualchannels.h)
description: This service is used to create a visual mapping on the client corresponding to a mapped window on the server.
helpviewer_keywords: ["IWTSBitmapRenderService","IWTSBitmapRenderService interface [Remote Desktop Services]","IWTSBitmapRenderService interface [Remote Desktop Services]","described","termserv.iwtsbitmaprenderservice","tsvirtualchannels/IWTSBitmapRenderService"]
old-location: termserv\iwtsbitmaprenderservice.htm
tech.root: TermServ
ms.assetid: 5ddc6ad8-1006-473e-b0f4-a5829045219a
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRenderService, IWTSBitmapRenderService interface [Remote Desktop Services], IWTSBitmapRenderService interface [Remote Desktop Services],described, termserv.iwtsbitmaprenderservice, tsvirtualchannels/IWTSBitmapRenderService
f1_keywords:
- tsvirtualchannels/IWTSBitmapRenderService
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
- IWTSBitmapRenderService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSBitmapRenderService interface


## -description


This service is used to create a visual mapping on the client corresponding to a mapped window on the server. The server-side mapped window is set using the <a href="https://docs.microsoft.com/windows/desktop/api/wtshintapi/nf-wtshintapi-wtssetrenderhint">WTSSetRenderHint</a> API.

This interface is implemented by the Remote Desktop Connection (RDC) client. You obtain an instance of this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtspluginserviceprovider-getservice">IWTSPluginServiceProvider::GetService</a> method, passing <b>RDCLIENT_BITMAP_RENDER_SERVICE</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSBitmapRenderService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSBitmapRenderService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSBitmapRenderService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderservice-getmappedrenderer">GetMappedRenderer</a>
</td>
<td align="left" width="63%">
Obtains the bitmap rendering object used to render media on the server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtspluginserviceprovider-getservice">IWTSPluginServiceProvider::GetService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtshintapi/nf-wtshintapi-wtssetrenderhint">WTSSetRenderHint</a>
 

 

