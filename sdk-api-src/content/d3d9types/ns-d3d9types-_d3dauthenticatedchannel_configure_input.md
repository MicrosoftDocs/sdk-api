---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
title: "_D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT"
author: windows-driver-content
description: Contains input data for the IDirect3DAuthenticatedChannel9::Configure method.
old-location: mf\d3dauthenticatedchannel_configure_input.htm
old-project: medfound
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT, D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT, mf.d3dauthenticatedchannel_configure_input
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
req.typenames: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT structure


## -description


Contains input data for the <a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a> method.


## -struct-fields




### -field omac

A <a href="https://msdn.microsoft.com/be5515fd-1936-46b8-9fc8-8d1f87048c38">D3D_OMAC</a> structure that contains a Message Authentication Code (MAC) of the data. The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.




### -field ConfigureType

A GUID that specifies the command. For a list of values, see <a href="https://msdn.microsoft.com/86be7dcf-7b7b-455a-a6ac-8a82b34fdafc">Content Protection Commands</a>.


### -field hChannel

A handle to the authenticated channel. To get the handle, call <a href="https://msdn.microsoft.com/e0dcfc3f-ede3-4917-8806-6bd343154cf8">IDirect3DDevice9Video::CreateAuthenticatedChannel</a>.




### -field SequenceNumber

The query sequence number. At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number. For each command, increment the sequence number by 1.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>
 

 

