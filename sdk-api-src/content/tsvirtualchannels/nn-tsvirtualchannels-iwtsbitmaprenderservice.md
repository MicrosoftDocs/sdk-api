---
UID: NN:tsvirtualchannels.IWTSBitmapRenderService
title: IWTSBitmapRenderService
author: windows-sdk-content
description: This service is used to create a visual mapping on the client corresponding to a mapped window on the server.
old-location: termserv\iwtsbitmaprenderservice.htm
old-project: termserv
ms.assetid: 5ddc6ad8-1006-473e-b0f4-a5829045219a
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IWTSBitmapRenderService, IWTSBitmapRenderService interface [Remote Desktop Services], IWTSBitmapRenderService interface [Remote Desktop Services],described, termserv.iwtsbitmaprenderservice, tsvirtualchannels/IWTSBitmapRenderService
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTSSBX_SESSION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tsvirtualchannels.h
api_name:
 - IWTSBitmapRenderService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSBitmapRenderService interface


## -description


This service is used to create a visual mapping on the client corresponding to a mapped window on the server. The server-side mapped window is set using the <a href="https://msdn.microsoft.com/CF8AE408-AE3A-44AC-91F9-6F6D9858893F">WTSSetRenderHint</a> API.

This interface is implemented by the Remote Desktop Connection (RDC) client. You obtain an instance of this interface by calling the <a href="https://msdn.microsoft.com/dd99c312-7899-4a94-ad40-abfd1a168332">IWTSPluginServiceProvider::GetService</a> method, passing <b>RDCLIENT_BITMAP_RENDER_SERVICE</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSBitmapRenderService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSBitmapRenderService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1a5f8ddb-eaf6-4138-8bb7-4d513aff88b5">GetMappedRenderer</a>
</td>
<td align="left" width="63%">
Obtains the bitmap rendering object used to render media on the server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dd99c312-7899-4a94-ad40-abfd1a168332">IWTSPluginServiceProvider::GetService</a>



<a href="https://msdn.microsoft.com/CF8AE408-AE3A-44AC-91F9-6F6D9858893F">WTSSetRenderHint</a>
 

 

