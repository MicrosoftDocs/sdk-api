---
UID: NF:tsvirtualchannels.IWTSPluginServiceProvider.GetService
title: IWTSPluginServiceProvider::GetService
author: windows-sdk-content
description: Obtains the specified service.
old-location: termserv\iwtspluginserviceprovider_getservice.htm
tech.root: termserv
ms.assetid: dd99c312-7899-4a94-ad40-abfd1a168332
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetService, GetService method [Remote Desktop Services], GetService method [Remote Desktop Services],IWTSPluginServiceProvider interface, IWTSPluginServiceProvider interface [Remote Desktop Services],GetService method, IWTSPluginServiceProvider.GetService, IWTSPluginServiceProvider::GetService, RDCLIENT_BITMAP_RENDER_SERVICE, termserv.iwtspluginserviceprovider_getservice, tsvirtualchannels/IWTSPluginServiceProvider::GetService
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
 - IWTSPluginServiceProvider.GetService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tsvirtualchannels.h
: 
- IWTSPluginServiceProvider.GetService
: 
---

# IWTSPluginServiceProvider::GetService


## -description


Obtains the specified service.


## -parameters




### -param ServiceId [in]

Specifies the service to retrieve. This can be the following values.



#### RDCLIENT_BITMAP_RENDER_SERVICE

Identifies the bitmap rendering service. The <i>ppunkObject</i> parameter receives an <a href="https://msdn.microsoft.com/5ddc6ad8-1006-473e-b0f4-a5829045219a">IWTSBitmapRenderService</a> interface pointer.


### -param ppunkObject [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that receives the service object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8baf8d8b-95a0-46bd-81ea-e99a7db45cdc">IWTSPluginServiceProvider</a>
 

 

