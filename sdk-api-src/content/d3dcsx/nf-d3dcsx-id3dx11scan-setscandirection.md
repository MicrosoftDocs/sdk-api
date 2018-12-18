---
UID: NF:d3dcsx.ID3DX11Scan.SetScanDirection
title: ID3DX11Scan::SetScanDirection
author: windows-sdk-content
description: Sets which direction to perform scans in.
old-location: direct3d11\id3dx11scan_setscandirection.htm
tech.root: direct3d11
ms.assetid: f26b0e71-0803-4c57-b1bc-cefad5c449b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3DX11Scan interface [Direct3D 11],SetScanDirection method, ID3DX11Scan.SetScanDirection, ID3DX11Scan::SetScanDirection, SetScanDirection, SetScanDirection method [Direct3D 11], SetScanDirection method [Direct3D 11],ID3DX11Scan interface, d3dcsx/ID3DX11Scan::SetScanDirection, direct3d11.id3dx11scan_setscandirection, f86c1216-b196-31a2-2a44-3b56262de095
ms.topic: method
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
 - COM
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - ID3DX11Scan.SetScanDirection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11Scan::SetScanDirection


## -description


Sets which direction to perform scans in.


## -parameters




### -param Direction [in]

Type: <b><a href="https://msdn.microsoft.com/bb2660c8-2a29-4eb2-9156-5516b60a8dc3">D3DX11_SCAN_DIRECTION</a></b>

Direction to perform scans in.  See <a href="https://msdn.microsoft.com/bb2660c8-2a29-4eb2-9156-5516b60a8dc3">D3DX11_SCAN_DIRECTION</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<b>SetScanDirection</b> sets the direction <a href="https://msdn.microsoft.com/42b91efd-3d84-4c76-bb9f-da0f398da6c7">ID3DX11Scan::Scan</a> and <a href="https://msdn.microsoft.com/5b6c637b-747d-465c-8915-dba13725ee0b">ID3DX11Scan::Multiscan</a> will performed scans in.




## -see-also




<a href="https://msdn.microsoft.com/f57401b9-fa1e-4470-a974-825749773f95">ID3DX11Scan</a>
 

 

