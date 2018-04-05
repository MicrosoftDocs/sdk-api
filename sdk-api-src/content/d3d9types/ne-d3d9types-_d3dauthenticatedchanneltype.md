---
UID: NE:d3d9types._D3DAUTHENTICATEDCHANNELTYPE
title: "_D3DAUTHENTICATEDCHANNELTYPE"
author: windows-driver-content
description: Specifies the type of Direct3D authenticated channel.
old-location: mf\d3dauthenticatedchanneltype.htm
old-project: medfound
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNELTYPE, D3DAUTHENTICATEDCHANNELTYPE enumeration [Media Foundation], D3DAUTHENTICATEDCHANNEL_D3D9, D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE, D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE, _D3DAUTHENTICATEDCHANNELTYPE, d3d9types/D3DAUTHENTICATEDCHANNELTYPE, d3d9types/D3DAUTHENTICATEDCHANNEL_D3D9, d3d9types/D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE, d3d9types/D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE, mf.d3dauthenticatedchanneltype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
req.include-header: D3d9.h
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
req.typenames: D3DAUTHENTICATEDCHANNELTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNELTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNELTYPE enumeration


## -description


Specifies the type of Direct3D authenticated channel.


## -enum-fields




### -field D3DAUTHENTICATEDCHANNEL_D3D9

Direct3D 9 channel. This channel provides communication with the Direct3D runtime.


### -field D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE

Software driver channel. This channel provides communication with a driver that implements content protection mechanisms in software.


### -field D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE

Hardware driver channel. This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.


## -see-also




<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/e0dcfc3f-ede3-4917-8806-6bd343154cf8">IDirect3DDevice9Video::CreateAuthenticatedChannel</a>
 

 

