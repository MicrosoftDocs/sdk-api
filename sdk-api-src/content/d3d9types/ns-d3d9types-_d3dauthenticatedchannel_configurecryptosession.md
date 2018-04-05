---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
title: "_D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION"
author: windows-driver-content
description: Contains input data for a D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION command.
old-location: mf\d3dauthenticatedchannel_configurecryptosession.htm
old-project: medfound
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION, D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION, d3d9types/D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION, mf.d3dauthenticatedchannel_configurecryptosession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION structure


## -description


Contains input data for a <a href="https://msdn.microsoft.com/d40fead7-8a86-426e-933e-13df21cdf50b">D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION</a> command.

To send this query, call <a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/7646100e-f768-4935-9e71-1d9db0d69c52">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.


### -field DXVA2DecodeHandle

A handle to the DirectX Video Acceleration 2 (DXVA-2) decoder device.


### -field CryptoSessionHandle

A handle to the cryptographic session.


### -field DeviceHandle

A handle to the Direct3D device.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>
 

 

