---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
title: "_D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE"
author: windows-driver-content
description: Contains input data for a D3DAUTHENTICATEDCONFIGURE_INITIALIZE command.
old-location: mf\d3dauthenticatedchannel_configureinitialize.htm
old-project: medfound
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE, D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE, d3d9types/D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE, mf.d3dauthenticatedchannel_configureinitialize
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
req.typenames: D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE structure


## -description


Contains input data for a <a href="https://msdn.microsoft.com/a74edbaa-af57-4f8e-9974-f6053f59377f">D3DAUTHENTICATEDCONFIGURE_INITIALIZE</a> command.

To send this query, call <a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/7646100e-f768-4935-9e71-1d9db0d69c52">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.


### -field StartSequenceQuery

The initial sequence number for queries.


### -field StartSequenceConfigure

The initial sequence number for commands.


## -remarks



The <b>StartSequenceQuery</b> and <b>StartSequenceConfigure</b> members each contain a cryptographically secure 32-bit random number. 




## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>
 

 

