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

# ID3D10Device::RSGetViewports


## -description


Get the array of <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">viewports</a> bound 
    to the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a>



## -parameters




### -param NumViewports [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Number of viewports in <i>pViewports</i>.  
        If <i>pViewports</i> is <b>NULL</b>, this will be filled with the number of viewports currently bound.


### -param pViewports [out]

Type: <b><a href="https://msdn.microsoft.com/3df8e77a-d85f-47cf-9796-03cf8ca6ed46">D3D10_VIEWPORT</a>*</b>

An array of viewports (see <a href="https://msdn.microsoft.com/3df8e77a-d85f-47cf-9796-03cf8ca6ed46">D3D10_VIEWPORT</a>) to be filled with information from the device. If NumViewports is greater than 
        the actual number of viewports currently bound, then unused members of the array will contain 0.


## -returns



Returns nothing.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

