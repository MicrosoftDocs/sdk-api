---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
title: "_D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION"
author: windows-driver-content
description: Contains input data for a D3DAUTHENTICATEDCONFIGURE_PROTECTION command.
old-location: mf\d3dauthenticatedchannel_configureprotection.htm
old-project: medfound
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION, D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION, d3d9types/D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION, mf.d3dauthenticatedchannel_configureprotection
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
req.typenames: D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION structure


## -description


Contains input data for a <a href="https://msdn.microsoft.com/120d940f-39a0-4ad5-bd3e-c108b3f98ace">D3DAUTHENTICATEDCONFIGURE_PROTECTION</a> command.

To send this query, call <a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/7646100e-f768-4935-9e71-1d9db0d69c52">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.


### -field Protections

A <a href="https://msdn.microsoft.com/681c6ad9-cf55-47e4-bbb9-e7fdc499a709">D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS</a> structure that specifies the protection level.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>
 

 

