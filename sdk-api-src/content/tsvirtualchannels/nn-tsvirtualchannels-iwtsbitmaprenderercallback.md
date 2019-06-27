---
UID: NN:tsvirtualchannels.IWTSBitmapRendererCallback
title: IWTSBitmapRendererCallback (tsvirtualchannels.h)
author: windows-sdk-content
description: A dynamic virtual channel plug-in implements this interface to be notified when the size of the rendering area changes.
old-location: termserv\iwtsbitmaprenderercallback.htm
tech.root: TermServ
ms.assetid: bdb8280b-6ebc-47e4-9789-47e3bda96efc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRendererCallback, IWTSBitmapRendererCallback interface [Remote Desktop Services], IWTSBitmapRendererCallback interface [Remote Desktop Services],described, termserv.iwtsbitmaprenderercallback, tsvirtualchannels/IWTSBitmapRendererCallback
ms.topic: interface
f1_keywords: 
 - "tsvirtualchannels/IWTSBitmapRendererCallback"
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
 - IWTSBitmapRendererCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSBitmapRendererCallback interface


## -description


A dynamic virtual channel plug-in implements this interface to be notified when the size of  the rendering area changes. A pointer to this interface is provided to the rendering service by using the <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderservice-getmappedrenderer">IWTSBitmapRenderService::GetMappedRenderer</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSBitmapRendererCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSBitmapRendererCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSBitmapRendererCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderercallback-ontargetsizechanged">OnTargetSizeChanged</a>
</td>
<td align="left" width="63%">
Called when the size of the render target has changed.

</td>
</tr>
</table> 

