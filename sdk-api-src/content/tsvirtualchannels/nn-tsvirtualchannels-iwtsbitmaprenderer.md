---
UID: NN:tsvirtualchannels.IWTSBitmapRenderer
title: IWTSBitmapRenderer (tsvirtualchannels.h)
author: windows-sdk-content
description: Used by a dynamic virtual channel plug-in to render bitmaps.
old-location: termserv\iwtsbitmaprenderer.htm
tech.root: TermServ
ms.assetid: 6930683e-bb9e-499c-b44f-27938faff3db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRenderer, IWTSBitmapRenderer interface [Remote Desktop Services], IWTSBitmapRenderer interface [Remote Desktop Services],described, termserv.iwtsbitmaprenderer, tsvirtualchannels/IWTSBitmapRenderer
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSBitmapRenderer interface


## -description


Used by a dynamic virtual channel plug-in to render bitmaps. This interface is implemented by the rendering service. The plug-in obtains a pointer to this interface by using the <a href="https://msdn.microsoft.com/1a5f8ddb-eaf6-4138-8bb7-4d513aff88b5">IWTSBitmapRenderService::GetMappedRenderer</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSBitmapRenderer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSBitmapRenderer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9BC4C091-053E-4E94-BF65-91AEB03C355F">GetRendererStatistics</a>
</td>
<td align="left" width="63%">
Retrieves statistics for the RemoteFX media redirection bitmap renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7961ba11-4ef8-4b08-8c50-68bd26999dc2">RemoveMapping</a>
</td>
<td align="left" width="63%">
Called by a dynamic virtual channel plug-in to remove a render mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/536c6954-0cde-48d1-ba5b-a97c9942f0f6">Render</a>
</td>
<td align="left" width="63%">
Called by a dynamic virtual channel plug-in to render bitmaps.

</td>
</tr>
</table> 

