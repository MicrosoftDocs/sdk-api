---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
title: "_D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION"
author: windows-driver-content
description: Contains input data for the D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE command.
old-location: mf\d3dauthenticatedchannel_configureuncompressedencryption.htm
old-project: medfound
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION, D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION, d3d9types/D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION, mf.d3dauthenticatedchannel_configureuncompressedencryption
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
req.typenames: D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION structure


## -description


Contains input data for the <a href="https://msdn.microsoft.com/6de6c4a3-705a-4420-b9f4-8d4d442b23bf">D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE</a> command.

To send this query, call <a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/7646100e-f768-4935-9e71-1d9db0d69c52">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.


### -field EncryptionGuid

A GUID that specifies the type of encryption to apply.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>
 

 

