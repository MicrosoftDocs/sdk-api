---
UID: NN:tsvirtualchannels.IWTSBitmapRenderer
title: IWTSBitmapRenderer (tsvirtualchannels.h)
description: Used by a dynamic virtual channel plug-in to render bitmaps.
helpviewer_keywords: ["IWTSBitmapRenderer","IWTSBitmapRenderer interface [Remote Desktop Services]","IWTSBitmapRenderer interface [Remote Desktop Services]","described","termserv.iwtsbitmaprenderer","tsvirtualchannels/IWTSBitmapRenderer"]
old-location: termserv\iwtsbitmaprenderer.htm
tech.root: TermServ
ms.assetid: 6930683e-bb9e-499c-b44f-27938faff3db
ms.date: 12/05/2018
ms.keywords: IWTSBitmapRenderer, IWTSBitmapRenderer interface [Remote Desktop Services], IWTSBitmapRenderer interface [Remote Desktop Services],described, termserv.iwtsbitmaprenderer, tsvirtualchannels/IWTSBitmapRenderer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSBitmapRenderer
 - tsvirtualchannels/IWTSBitmapRenderer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tsvirtualchannels.h
api_name:
 - IWTSBitmapRenderer
---

# IWTSBitmapRenderer interface


## -description

Used by a dynamic virtual channel plug-in to render bitmaps. This interface is implemented by the rendering service. The plug-in obtains a pointer to this interface by using the <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderservice-getmappedrenderer">IWTSBitmapRenderService::GetMappedRenderer</a> method.

## -inheritance

The <b>IWTSBitmapRenderer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSBitmapRenderer</b> also has these types of members:

