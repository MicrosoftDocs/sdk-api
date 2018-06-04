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

# ID3D11Linker::AddClipPlaneFromCBuffer


## -description


Adds a <a href="https://msdn.microsoft.com/C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11">clip plane</a> with the plane coefficients taken from a <a href="https://msdn.microsoft.com/89fe874a-8009-4901-bebe-2d9e45f894bb">cbuffer</a> entry for 10Level9 shaders.


## -parameters




### -param uCBufferSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The <a href="https://msdn.microsoft.com/89fe874a-8009-4901-bebe-2d9e45f894bb">cbuffer</a> slot number.


### -param uCBufferEntry [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The <a href="https://msdn.microsoft.com/89fe874a-8009-4901-bebe-2d9e45f894bb">cbuffer</a> entry number.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/08967A5F-AAAE-4352-A8A9-C7B1ED16EF25">ID3D11Linker</a>
 

 

