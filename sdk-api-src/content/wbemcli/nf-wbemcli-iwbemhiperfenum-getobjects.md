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

# IWbemHiPerfEnum::GetObjects


## -description


The 
<b>IWbemHiPerfEnum::GetObjects</b> method retrieves objects currently residing in the enumerator.


## -parameters




### -param lFlags [in]

Integer that contains the flags.


### -param uNumObjects [in]

Size of the array passed to this method in the <i>apObj</i> parameter.


### -param apObj [out]

Pointer that holds the reference to an array of 
<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a> objects, which contains the returned objects. The array must be big enough to hold all objects in the enumerator.


### -param puReturned [out]

Pointer to a <b>ULONG</b> used to return the number of objects placed in the array.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The array must be large enough to hold all objects, or <i>puReturned</i> is filled with the number of returned objects, and <b>WBEM_E_BUFFER_TOO_SMALL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfEnum</a>
 

 

