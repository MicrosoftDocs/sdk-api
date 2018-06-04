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

# ID3D11Device3::CreateQuery1


## -description


Creates a query object for querying information from the graphics processing unit (GPU). 


## -parameters




### -param pQueryDesc1 [in]

Type: <b>const <a href="https://msdn.microsoft.com/56FFA63E-E7C6-45A4-80E9-B12E9042AE13">D3D11_QUERY_DESC1</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/56FFA63E-E7C6-45A4-80E9-B12E9042AE13">D3D11_QUERY_DESC1</a> structure that represents a query description.


### -param ppQuery1 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/6DF4364F-A20D-466E-8F26-17C6DD32E84B">ID3D11Query1</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/6DF4364F-A20D-466E-8F26-17C6DD32E84B">ID3D11Query1</a> interface for the created query object. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the query object.  
        See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.




## -see-also




<a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>
 

 

