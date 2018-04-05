---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
title: "_D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT"
author: windows-driver-content
description: Contains the response to a call to the IDirect3DAuthenticatedChannel9::Configure method.
old-location: mf\d3dauthenticatedchannel_configure_output.htm
old-project: medfound
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT, D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT, mf.d3dauthenticatedchannel_configure_output
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
req.typenames: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT structure


## -description


Contains the response to a call to the <a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a> method.


## -struct-fields




### -field omac

A <a href="https://msdn.microsoft.com/be5515fd-1936-46b8-9fc8-8d1f87048c38">D3D_OMAC</a> structure that contains a Message Authentication Code (MAC) of the data. The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.




### -field ConfigureType

A GUID that specifies the command. For a list of values, see <a href="https://msdn.microsoft.com/86be7dcf-7b7b-455a-a6ac-8a82b34fdafc">Content Protection Commands</a>.


### -field hChannel

A handle to the authenticated channel.


### -field SequenceNumber

The command sequence number.


### -field ReturnCode

The result code for the command.


## -remarks



For the <b>ConfigureType</b>, <b>hChannel</b>, and <b>SequenceNumber</b> members, the driver uses the same values that the application provided in the <a href="https://msdn.microsoft.com/7646100e-f768-4935-9e71-1d9db0d69c52">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure. The application should verify that these values match.






## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>
 

 

