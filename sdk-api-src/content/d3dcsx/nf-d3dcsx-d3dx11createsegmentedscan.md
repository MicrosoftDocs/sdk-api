---
UID: NF:d3dcsx.D3DX11CreateSegmentedScan
title: D3DX11CreateSegmentedScan function
author: windows-sdk-content
description: Creates a segmented scan context.
old-location: direct3d11\d3dx11createsegmentedscan.htm
old-project: direct3d11
ms.assetid: f8906357-57d8-4e57-a120-2ac28fad2288
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 6b834305-1925-9f3d-ee71-8dc858a331c0, D3DX11CreateSegmentedScan, D3DX11CreateSegmentedScan function [Direct3D 11], d3dcsx/D3DX11CreateSegmentedScan, direct3d11.d3dx11createsegmentedscan
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3dcsx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3DX11_SCAN_OPCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - D3DX11CreateSegmentedScan
product: Windows
targetos: Windows
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
---

# D3DX11CreateSegmentedScan function


## -description


Creates a segmented scan context.


## -parameters




### -param pDeviceContext [in]

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> interface.
          


### -param MaxElementScanSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Maximum single scan size, in elements (FLOAT, UINT, or INT).


### -param ppScan [out]

Type: <b><a href="https://msdn.microsoft.com/58d8d3ea-25d6-4767-9693-fbc97ae3e8b8">ID3DX11SegmentedScan</a>**</b>

Pointer to a <a href="https://msdn.microsoft.com/58d8d3ea-25d6-4767-9693-fbc97ae3e8b8">ID3DX11SegmentedScan Interface</a> pointer that will be set to the created interface object.
            


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

The return value is one of the values listed in <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/426A132F-E398-473E-BD4E-3D1B4EC92E3F">D3DCSX 11 Functions</a>
 

 

