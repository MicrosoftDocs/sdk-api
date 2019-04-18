---
UID: NF:dxva2api.DXVA2CreateVideoService
title: DXVA2CreateVideoService function (dxva2api.h)
author: windows-sdk-content
description: Creates a DirectX Video Acceleration (DXVA) services object.
old-location: mf\dxva2createvideoservice.htm
tech.root: medfound
ms.assetid: e62dbacb-f638-4307-ba56-88415d881fc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXVA2CreateVideoService, DXVA2CreateVideoService function [Media Foundation], dxva2api/DXVA2CreateVideoService, e62dbacb-f638-4307-ba56-88415d881fc9, mf.dxva2createvideoservice
ms.topic: function
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - DXVA2CreateVideoService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DXVA2CreateVideoService function


## -description


Creates a DirectX Video Acceleration (DXVA) services object. Call this function if your application uses DXVA directly, without using DirectShow or Media Foundation.
        
      


## -parameters




### -param pDD

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a> interface of a Direct3D device.
          


### -param riid

The interface identifier (IID) of the requested interface. Any of the following interfaces might be supported by the Direct3D device:
          

<ul>
<li>
<a href="https://msdn.microsoft.com/50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17">IDirectXVideoAccelerationService</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eeb62178-b54d-45d3-a584-75865f0662fa">IDirectXVideoDecoderService</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688">IDirectXVideoProcessorService</a>
</li>
</ul>

### -param ppService

Receives a pointer to the interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

