---
UID: NF:d3dcsx.ID3DX11SegmentedScan.SetScanDirection
title: ID3DX11SegmentedScan::SetScanDirection method
author: windows-driver-content
description: Sets which direction to perform scans in.
old-location: direct3d11\id3dx11segmentedscan_setscandirection.htm
old-project: direct3d11
ms.assetid: 84eca342-33a3-4595-adb2-0a39e6060e49
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3DX11SegmentedScan, ID3DX11SegmentedScan interface [Direct3D 11], SetScanDirection method, ID3DX11SegmentedScan::SetScanDirection, SetScanDirection method [Direct3D 11], SetScanDirection method [Direct3D 11], ID3DX11SegmentedScan interface, SetScanDirection,ID3DX11SegmentedScan.SetScanDirection, a63add8c-ff04-6737-e439-b59bf93546a1, d3dcsx/ID3DX11SegmentedScan::SetScanDirection, direct3d11.id3dx11segmentedscan_setscandirection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3DX11_SCAN_OPCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3dcsx.lib
-	d3dcsx.dll
api_name:
-	ID3DX11SegmentedScan.SetScanDirection
product: Windows
targetos: Windows
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
---

# ID3DX11SegmentedScan::SetScanDirection method


## -description


Sets which direction to perform scans in.


## -parameters




### -param Direction [in]

Type: <b><a href="https://msdn.microsoft.com/bb2660c8-2a29-4eb2-9156-5516b60a8dc3">D3DX11_SCAN_DIRECTION</a></b>

Direction to perform scans in.  See <a href="https://msdn.microsoft.com/bb2660c8-2a29-4eb2-9156-5516b60a8dc3">D3DX11_SCAN_DIRECTION</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<b>SetScanDirection</b> sets the direction <a href="https://msdn.microsoft.com/096e1cc1-0bab-4e23-8c4c-47a2a0ff49fb">ID3DX11SegmentedScan::SegScan</a> will performed scans in.




## -see-also




<a href="https://msdn.microsoft.com/58d8d3ea-25d6-4767-9693-fbc97ae3e8b8">ID3DX11SegmentedScan</a>
 

 

