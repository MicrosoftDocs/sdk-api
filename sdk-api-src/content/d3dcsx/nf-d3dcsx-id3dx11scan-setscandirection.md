---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3DX11Scan::SetScanDirection


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



<b>SetScanDirection</b> sets the direction <a href="https://msdn.microsoft.com/42b91efd-3d84-4c76-bb9f-da0f398da6c7">ID3DX11Scan::Scan</a> and <a href="https://msdn.microsoft.com/5b6c637b-747d-465c-8915-dba13725ee0b">ID3DX11Scan::Multiscan</a> will performed scans in.




## -see-also




<a href="https://msdn.microsoft.com/f57401b9-fa1e-4470-a974-825749773f95">ID3DX11Scan</a>
 

 

