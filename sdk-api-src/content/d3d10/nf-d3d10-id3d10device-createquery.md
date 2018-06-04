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

# ID3D10Device::CreateQuery


## -description


This interface encapsulates methods for querying information from the GPU.


## -parameters




### -param pQueryDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/50fab3df-78f7-4bac-b353-0e840873f13e">D3D10_QUERY_DESC</a>*</b>

Pointer to a query description (see <a href="https://msdn.microsoft.com/50fab3df-78f7-4bac-b353-0e840873f13e">D3D10_QUERY_DESC</a>).


### -param ppQuery [out]

Type: <b><a href="https://msdn.microsoft.com/ffa69b76-ce8d-4386-b0be-fecada85d37c">ID3D10Query</a>**</b>

Address of a pointer to the query object created (see <a href="https://msdn.microsoft.com/ffa69b76-ce8d-4386-b0be-fecada85d37c">ID3D10Query Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

