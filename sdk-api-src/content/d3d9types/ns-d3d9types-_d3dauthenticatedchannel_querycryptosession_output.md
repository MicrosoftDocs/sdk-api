---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
title: "_D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT"
author: windows-driver-content
description: Contains the response to a D3DAUTHENTICATEDQUERY_CRYPTOSESSION query.
old-location: mf\d3dauthenticatedchannel_querycryptosession_output.htm
old-project: medfound
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT, D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT, mf.d3dauthenticatedchannel_querycryptosession_output
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
req.typenames: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT structure


## -description


Contains the response to a <a href="https://msdn.microsoft.com/90b3bcf3-2988-48de-8acd-62e385d4fdf0">D3DAUTHENTICATEDQUERY_CRYPTOSESSION</a> query.

To send this query, call <a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>.


## -struct-fields




### -field Output

A <a href="https://msdn.microsoft.com/b2783b8e-0436-419a-a93e-93dc1b87024d">D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.


### -field DXVA2DecodeHandle

A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.


### -field CryptoSessionHandle

A handle to the cryptographic session that is associated with the decoder device.


### -field DeviceHandle

A handle to the Direct3D device that is associated with the decoder device.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>
 

 

