---
UID: NF:dxva.IDirect3DVideoDevice9.CreateDXVADevice
title: IDirect3DVideoDevice9::CreateDXVADevice method
author: windows-driver-content
description: Creates a DirectX Video Acceleration (DXVA) decoder device.
old-location: mf\idirect3dvideodevice9_createdxvadevice.htm
old-project: medfound
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: CreateDXVADevice method [Media Foundation], CreateDXVADevice method [Media Foundation], IDirect3DVideoDevice9 interface, CreateDXVADevice,IDirect3DVideoDevice9.CreateDXVADevice, IDirect3DVideoDevice9, IDirect3DVideoDevice9 interface [Media Foundation], CreateDXVADevice method, IDirect3DVideoDevice9::CreateDXVADevice, dxva/IDirect3DVideoDevice9::CreateDXVADevice, mf.idirect3dvideodevice9_createdxvadevice
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
-	IDirect3DVideoDevice9.CreateDXVADevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DVideoDevice9::CreateDXVADevice method


## -description


Creates a DirectX Video Acceleration (DXVA) decoder device.


## -parameters




### -param pGuid

Pointer to a GUID that specifies the device to create.


### -param pUncompData

Pointer to a <a href="https://msdn.microsoft.com/bd19d9a8-7d69-4aea-9638-84c3f1a1e810">DXVAUncompDataInfo</a> structure that specifies the format of the uncompressed image.


### -param pData

Pointer to a <b>DXVA_ConnectMode</b>  structure that specifies the DXVA mode and restricted profile.


### -param DataSize

Size of the <b>DXVA_ConnectMode</b>  structure, in bytes.


### -param ppDXVADevice

Receives a pointer to the <a href="https://msdn.microsoft.com/63f77cf9-4c04-4ddb-9582-cfcf86f66a2a">IDirect3DDXVADevice9</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/abe3beac-f3f8-413d-8b83-9da3340b19ac">IDirect3DVideoDevice9</a>
 

 

