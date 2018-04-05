---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
title: "_D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT"
author: windows-driver-content
description: Contains the response from the IDirect3DAuthenticatedChannel9::Query method.
old-location: mf\d3dauthenticatedchannel_query_output.htm
old-project: medfound
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT, D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT, mf.d3dauthenticatedchannel_query_output
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
req.typenames: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT structure


## -description


Contains the response from the <a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a> method.


## -struct-fields




### -field omac

A <a href="https://msdn.microsoft.com/be5515fd-1936-46b8-9fc8-8d1f87048c38">D3D_OMAC</a> structure that contains a Message Authentication Code (MAC) of the data. The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.


### -field QueryType

A GUID that specifies the query. For a list of values, see <a href="https://msdn.microsoft.com/75e246c6-bf23-44d9-8fb3-46a6dc5324a5">Content Protection Queries</a>.


### -field hChannel

 


### -field SequenceNumber

 


### -field ReturnCode

The result code for the query.


#### - HANDLE

A handle to the authenticated channel.


#### - UINT

The query sequence number.


## -remarks



For the <b>QueryType</b>, <b>hChannel</b>, and <b>SequenceNumber</b> members, the driver uses in the same values that the application provided in the <a href="https://msdn.microsoft.com/6a484652-8da2-4074-96b2-6fe49f4d4200">D3DAUTHENTICATEDCHANNEL_QUERY_INPUT</a> structure. The application should verify that these values match.




## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>
 

 

