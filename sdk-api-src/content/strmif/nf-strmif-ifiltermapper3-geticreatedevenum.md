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

# IFilterMapper3::GetICreateDevEnum


## -description



The <code>GetICreateDevEnum</code> method returns a pointer to the <b>ICreateDevEnum</b> interface. You can use the <a href="https://msdn.microsoft.com/fc300bb8-aea4-4848-af43-a70a7fb8c07c">ICreateDevEnum</a> interface to create an enumerator for a category of filters, such as video capture devices or audio capture devices.


<div class="alert"><b>Note</b>  This method is deprecated. Instead, applications should call <b>CoCreateInstance</b> with CLSID_SystemDeviceEnum to create the <a href="https://msdn.microsoft.com/ea98be7f-580d-4986-bd6b-d254a2c075e8">System Device Enumerator</a>.</div><div> </div>

## -parameters




### -param ppEnum [out]

Receives a pointer to the <b>ICreateDevEnum</b> interface. The caller must release the interface.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/385a4d15-08b5-40c6-8444-a22bec86a981">IFilterMapper3 Interface</a>
 

 

