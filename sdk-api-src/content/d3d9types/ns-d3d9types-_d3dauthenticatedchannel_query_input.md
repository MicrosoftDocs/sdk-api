---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
title: "_D3DAUTHENTICATEDCHANNEL_QUERY_INPUT"
author: windows-driver-content
description: Contains input data for the IDirect3DAuthenticatedChannel9::Query method.
old-location: mf\d3dauthenticatedchannel_query_input.htm
old-project: medfound
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_QUERY_INPUT, D3DAUTHENTICATEDCHANNEL_QUERY_INPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_QUERY_INPUT, mf.d3dauthenticatedchannel_query_input
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
req.typenames: D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT structure


## -description


Contains input data for the <a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a> method.


## -struct-fields




### -field QueryType

A GUID that specifies the query. For a list of values, see <a href="https://msdn.microsoft.com/75e246c6-bf23-44d9-8fb3-46a6dc5324a5">Content Protection Queries</a>.


### -field hChannel

 


### -field SequenceNumber

 




#### - HANDLE

A handle to the authenticated channel. To get the handle, call <a href="https://msdn.microsoft.com/e0dcfc3f-ede3-4917-8806-6bd343154cf8">IDirect3DDevice9Video::CreateAuthenticatedChannel</a>.


#### - UINT

The query sequence number. At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number. For each query, increment the sequence number by 1.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>
 

 

