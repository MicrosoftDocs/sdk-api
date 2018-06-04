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
 

 

