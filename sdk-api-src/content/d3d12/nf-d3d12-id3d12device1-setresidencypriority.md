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

# ID3D12Device1::SetResidencyPriority


## -description



This method sets residency priorities of a specified list of objects.




## -parameters




### -param NumObjects

Type: <b>UINT</b>

Specifies the number of objects in the <i>ppObjects</i> and <i>pPriorities</i> arrays.


### -param ppObjects [in]

Type: <b>ID3D12Pageable*</b>

Specifies an array, of length <i>NumObjects</i>, containing references to <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a> objects.


### -param pPriorities [in]

Type: <b>const <a href="https://msdn.microsoft.com/40A38135-D974-4A35-8859-6F9FE21FAC8D">D3D12_RESIDENCY_PRIORITY</a>*</b>

Specifies an array, of length <i>NumObjects</i>, of <a href="https://msdn.microsoft.com/40A38135-D974-4A35-8859-6F9FE21FAC8D">D3D12_RESIDENCY_PRIORITY</a> values for the list of objects.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



For more information, refer to <a href="https://msdn.microsoft.com/956F80D7-EEC8-4D88-B251-EE325614F31E">Residency</a>.




## -see-also




<a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>
 

 

