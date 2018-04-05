---
UID: NF:dxva.IDirect3DVideoDevice9.GetDXVAInternalInfo
title: IDirect3DVideoDevice9::GetDXVAInternalInfo method
author: windows-driver-content
description: Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.
old-location: mf\idirect3dvideodevice9_getdxvainternalinfo.htm
old-project: medfound
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetDXVAInternalInfo method [Media Foundation], GetDXVAInternalInfo method [Media Foundation], IDirect3DVideoDevice9 interface, GetDXVAInternalInfo,IDirect3DVideoDevice9.GetDXVAInternalInfo, IDirect3DVideoDevice9, IDirect3DVideoDevice9 interface [Media Foundation], GetDXVAInternalInfo method, IDirect3DVideoDevice9::GetDXVAInternalInfo, dxva/IDirect3DVideoDevice9::GetDXVAInternalInfo, mf.idirect3dvideodevice9_getdxvainternalinfo
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
-	IDirect3DVideoDevice9.GetDXVAInternalInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DVideoDevice9::GetDXVAInternalInfo method


## -description


Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use. 


## -parameters




### -param pGuid

Pointer to a GUID that specifies the DXVA profile. To get a list of supported profiles, call <a href="https://msdn.microsoft.com/4adbbac2-a25d-4e17-b62e-a02a67dcdbed">IDirect3DVideoDevice9::GetDXVAGuids</a>.


### -param pUncompData

Pointer to a <a href="https://msdn.microsoft.com/bd19d9a8-7d69-4aea-9638-84c3f1a1e810">DXVAUncompDataInfo</a> structure that specifies the size and pixel format of the uncompressed data.


### -param pMemoryUsed

Receives the amount of scratch memory that the HAL will allocate, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/abe3beac-f3f8-413d-8b83-9da3340b19ac">IDirect3DVideoDevice9</a>
 

 

