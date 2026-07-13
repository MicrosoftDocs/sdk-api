---
UID: NF:tsvirtualchannels.IWTSPluginServiceProvider.GetService
title: IWTSPluginServiceProvider::GetService (tsvirtualchannels.h)
description: Obtains the specified service.
helpviewer_keywords: ["GetService","GetService method [Remote Desktop Services]","GetService method [Remote Desktop Services]","IWTSPluginServiceProvider interface","IWTSPluginServiceProvider interface [Remote Desktop Services]","GetService method","IWTSPluginServiceProvider.GetService","IWTSPluginServiceProvider::GetService","RDCLIENT_BITMAP_RENDER_SERVICE","termserv.iwtspluginserviceprovider_getservice","tsvirtualchannels/IWTSPluginServiceProvider::GetService"]
old-location: termserv\iwtspluginserviceprovider_getservice.htm
tech.root: TermServ
ms.assetid: dd99c312-7899-4a94-ad40-abfd1a168332
ms.date: 12/05/2018
ms.keywords: GetService, GetService method [Remote Desktop Services], GetService method [Remote Desktop Services],IWTSPluginServiceProvider interface, IWTSPluginServiceProvider interface [Remote Desktop Services],GetService method, IWTSPluginServiceProvider.GetService, IWTSPluginServiceProvider::GetService, RDCLIENT_BITMAP_RENDER_SERVICE, termserv.iwtspluginserviceprovider_getservice, tsvirtualchannels/IWTSPluginServiceProvider::GetService
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
 - IWTSPluginServiceProvider::GetService
 - tsvirtualchannels/IWTSPluginServiceProvider::GetService
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
 - IWTSPluginServiceProvider.GetService
---

# IWTSPluginServiceProvider::GetService


## -description

Obtains the specified service.

## -parameters

### -param ServiceId [in]

Specifies the service to retrieve. This can be the following values.



#### RDCLIENT_BITMAP_RENDER_SERVICE

Identifies the bitmap rendering service. The <i>ppunkObject</i> parameter receives an <a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderservice">IWTSBitmapRenderService</a> interface pointer.

### -param ppunkObject [out]

The address of a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that receives the service object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtspluginserviceprovider">IWTSPluginServiceProvider</a>