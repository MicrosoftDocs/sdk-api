---
UID: NF:d3dcsx.D3DX11CreateScan
title: D3DX11CreateScan function
author: windows-sdk-content
description: Creates a scan context.
old-location: direct3d11\d3dx11createscan.htm
tech.root: direct3d11
ms.assetid: daaa6913-a952-4f89-8a17-17e690ad8883
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 084772c2-3360-63d5-fb00-82f536323a9d, D3DX11CreateScan, D3DX11CreateScan function [Direct3D 11], d3dcsx/D3DX11CreateScan, direct3d11.d3dx11createscan
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - D3DX11CreateScan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DX11CreateScan function


## -description


Creates a scan context.


## -parameters




### -param pDeviceContext [in]

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>*</b>

The <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> the scan is associated with.
          


### -param MaxElementScanSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Maximum single scan size, in elements (FLOAT, UINT, or INT).
          


### -param MaxScanCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Maximum number of scans in multiscan.
          


### -param ppScan [out]

Type: <b><a href="https://msdn.microsoft.com/f57401b9-fa1e-4470-a974-825749773f95">ID3DX11Scan</a>**</b>

Pointer to a <a href="https://msdn.microsoft.com/f57401b9-fa1e-4470-a974-825749773f95">ID3DX11Scan Interface</a> pointer that will be set to the created interface object.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

The return value is one of the values listed in <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/426A132F-E398-473E-BD4E-3D1B4EC92E3F">D3DCSX 11 Functions</a>
 

 

