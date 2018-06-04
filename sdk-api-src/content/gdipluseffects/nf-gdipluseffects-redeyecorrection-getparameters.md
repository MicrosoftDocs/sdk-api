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

# RedEyeCorrection::GetParameters


## -description


The <b>RedEyeCorrection::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a> object. 


## -parameters




### -param size [in]

Type: <b>UINT*</b>

The size, in bytes, of the buffer pointed to by the <i>parameters</i> parameter.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/5c4832f7-de89-4596-915f-2cd23b8c1c2f">RedEyeCorrectionParams</a>*</b>

Pointer to a buffer that is large enough to receive a <a href="https://msdn.microsoft.com/5c4832f7-de89-4596-915f-2cd23b8c1c2f">RedEyeCorrectionParams</a> structure followed by an array of RECT structures. To determine the total size of the required buffer, call the GetParameterSize method of the <a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a> object whose parameters you want to retrieve.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a>



<a href="https://msdn.microsoft.com/ed889acb-37c1-4fa6-9c46-1f41428b9b36">RedEyeCorrection::SetParameters</a>
 

 

