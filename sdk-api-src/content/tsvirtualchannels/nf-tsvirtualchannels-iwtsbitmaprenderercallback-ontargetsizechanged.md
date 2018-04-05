---
UID: NF:tsvirtualchannels.IWTSBitmapRendererCallback.OnTargetSizeChanged
title: IWTSBitmapRendererCallback::OnTargetSizeChanged method
author: windows-driver-content
description: Called when the size of the render target has changed.
old-location: termserv\iwtsbitmaprenderercallback_ontargetsizechanged.htm
old-project: TermServ
ms.assetid: 2c4eeec8-7d9c-4321-9fdb-3ea8c7a36893
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IWTSBitmapRendererCallback, IWTSBitmapRendererCallback interface [Remote Desktop Services], OnTargetSizeChanged method, IWTSBitmapRendererCallback::OnTargetSizeChanged, OnTargetSizeChanged method [Remote Desktop Services], OnTargetSizeChanged method [Remote Desktop Services], IWTSBitmapRendererCallback interface, OnTargetSizeChanged,IWTSBitmapRendererCallback.OnTargetSizeChanged, termserv.iwtsbitmaprenderercallback_ontargetsizechanged, tsvirtualchannels/IWTSBitmapRendererCallback::OnTargetSizeChanged
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
-	IWTSBitmapRendererCallback.OnTargetSizeChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSBitmapRendererCallback::OnTargetSizeChanged method


## -description


Called when the size of the render target has changed. The image passed to <a href="https://msdn.microsoft.com/536c6954-0cde-48d1-ba5b-a97c9942f0f6">IWTSBitmapRenderer::Render</a> must conform to this size.


## -parameters




### -param rcNewSize [in]

A <b>RECT</b> structure that contains the new size of the render target.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bdb8280b-6ebc-47e4-9789-47e3bda96efc">IWTSBitmapRendererCallback</a>
 

 

