---
UID: NF:dxva.IDirect3DDXVADevice9.BeginFrame
title: IDirect3DDXVADevice9::BeginFrame method
author: windows-driver-content
description: Begins the processing to create a decoded picture.
old-location: mf\idirect3ddxvadevice9_beginframe.htm
old-project: medfound
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: BeginFrame method [Media Foundation], BeginFrame method [Media Foundation], IDirect3DDXVADevice9 interface, BeginFrame,IDirect3DDXVADevice9.BeginFrame, IDirect3DDXVADevice9, IDirect3DDXVADevice9 interface [Media Foundation], BeginFrame method, IDirect3DDXVADevice9::BeginFrame, dxva/IDirect3DDXVADevice9::BeginFrame, mf.idirect3ddxvadevice9_beginframe
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxva.h
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
req.typenames: COPP_TVProtectionStandard
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva.h
api_name:
-	IDirect3DDXVADevice9.BeginFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DDXVADevice9::BeginFrame method


## -description


Begins the processing to create a decoded picture.


## -parameters




### -param pDstSurface

A pointer to the <b>IDirect3DSurface9</b> interface of the uncompressed destination surface.


### -param SizeInputData

The size of the buffer specified by <i>pInputData</i>, in bytes. The value must be 2.


### -param pInputData

Pointer to a buffer that contains data for the video accelerator. This buffer must contain the zero-based frame index, specified as a <b>WORD</b> value. 


### -param pSizeOutputData

The size of the buffer specified by <i>pOutputData</i>, in bytes. The value must be zero.


### -param pOutputData

Pointer to a buffer that the video accelerator can write to. Set this parameter to <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For each call to <b>BeginFrame</b>, the decoder must make a corresponding call to <a href="https://msdn.microsoft.com/4b47cd53-6ce0-47b0-83ed-84926e92430f">IDirect3DDXVADevice9::EndFrame</a>.




## -see-also




<a href="https://msdn.microsoft.com/63f77cf9-4c04-4ddb-9582-cfcf86f66a2a">IDirect3DDXVADevice9</a>
 

 

