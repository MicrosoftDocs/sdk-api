---
UID: NF:tsvirtualchannels.IWTSBitmapRenderService.GetMappedRenderer
title: IWTSBitmapRenderService::GetMappedRenderer
author: windows-sdk-content
description: Obtains the bitmap rendering object used to render media on the server.
old-location: termserv\iwtsbitmaprenderservice_getmappedrenderer.htm
old-project: TermServ
ms.assetid: 1a5f8ddb-eaf6-4138-8bb7-4d513aff88b5
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetMappedRenderer, GetMappedRenderer method [Remote Desktop Services], GetMappedRenderer method [Remote Desktop Services],IWTSBitmapRenderService interface, IWTSBitmapRenderService interface [Remote Desktop Services],GetMappedRenderer method, IWTSBitmapRenderService.GetMappedRenderer, IWTSBitmapRenderService::GetMappedRenderer, termserv.iwtsbitmaprenderservice_getmappedrenderer, tsvirtualchannels/IWTSBitmapRenderService::GetMappedRenderer
ms.prod: windows
ms.technology: windows-sdk
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
 - IWTSBitmapRenderService.GetMappedRenderer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSBitmapRenderService::GetMappedRenderer


## -description


Obtains the bitmap rendering object used to render media on the server.


## -parameters




### -param mappingId [in]

A 64-bit number that uniquely identifies the render mapping.


### -param pMappedRendererCallback [in]

The address of the caller's <a href="https://msdn.microsoft.com/bdb8280b-6ebc-47e4-9789-47e3bda96efc">IWTSBitmapRendererCallback</a> interface.


### -param ppMappedRenderer [out]

The address of an <a href="https://msdn.microsoft.com/6930683e-bb9e-499c-b44f-27938faff3db">IWTSBitmapRenderer</a> interface pointer that receives the bitmap renderer. When you have finished using pointer, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release()</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5ddc6ad8-1006-473e-b0f4-a5829045219a">IWTSBitmapRenderService</a>
 

 

