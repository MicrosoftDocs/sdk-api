---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
title: "_D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT"
author: windows-driver-content
description: Contains input data for a D3DAUTHENTICATEDQUERY_CRYPTOSESSION query.
old-location: mf\d3dauthenticatedchannel_querycryptosession_input.htm
old-project: medfound
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT, D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT, mf.d3dauthenticatedchannel_querycryptosession_input
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
req.typenames: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT structure


## -description


Contains input data for a <a href="https://msdn.microsoft.com/90b3bcf3-2988-48de-8acd-62e385d4fdf0">D3DAUTHENTICATEDQUERY_CRYPTOSESSION</a> query.

To send this query, call <a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>.


## -struct-fields




### -field Input

A <a href="https://msdn.microsoft.com/6a484652-8da2-4074-96b2-6fe49f4d4200">D3DAUTHENTICATEDCHANNEL_QUERY_INPUT</a> structure that contains the GUID for the query and other data.


### -field DXVA2DecodeHandle

A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>
 

 

