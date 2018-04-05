---
UID: NF:dxva.IDirect3DDXVADevice9.EndFrame
title: IDirect3DDXVADevice9::EndFrame method
author: windows-driver-content
description: Ends the processing to create a decoded picture.
old-location: mf\idirect3ddxvadevice9_endframe.htm
old-project: medfound
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: EndFrame method [Media Foundation], EndFrame method [Media Foundation], IDirect3DDXVADevice9 interface, EndFrame,IDirect3DDXVADevice9.EndFrame, IDirect3DDXVADevice9, IDirect3DDXVADevice9 interface [Media Foundation], EndFrame method, IDirect3DDXVADevice9::EndFrame, dxva/IDirect3DDXVADevice9::EndFrame, mf.idirect3ddxvadevice9_endframe
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
-	IDirect3DDXVADevice9.EndFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DDXVADevice9::EndFrame method


## -description


Ends the processing to create a decoded picture.


## -parameters




### -param SizeMiscData

The size of the buffer specified by <i>pMiscData</i>, in bytes. The value must be 2.


### -param pMiscData

Pointer to a buffer that contains data for the video accelerator. This buffer must contain the same frame index that was passed to the <a href="https://msdn.microsoft.com/80471cc6-c66d-49d9-8593-780e41ac39b9">IDirect3DDXVADevice9::BeginFrame</a> method in the <i>pInputData</i> parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/63f77cf9-4c04-4ddb-9582-cfcf86f66a2a">IDirect3DDXVADevice9</a>
 

 

