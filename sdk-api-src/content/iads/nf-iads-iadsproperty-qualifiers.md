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

# IADsProperty::Qualifiers


## -description


The <b>IADsProperty::Qualifiers</b> method is an optional method that returns a collection of ADSI objects that describe additional qualifiers of this property.


## -parameters




### -param ppQualifiers [out]

Indirect pointer to the  <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> interface on the ADSI collection object that represents additional limits for this property.


## -returns



This method supports the standard return values <b>E_FAIL</b> and <b>E_UNEXPECTED</b>, as well as the following:




## -remarks



The qualifier objects are provider-specific. When supported, this method can be used to obtain extended schema data.

This method is not currently supported by any of the providers supplied by Microsoft.




## -see-also




<a href="https://msdn.microsoft.com/d05e4278-2dfb-4832-a97d-eb35253ae535">IADsClass::Qualifiers</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/ebf03974-371b-4bf4-91b4-f137339bd784">IADsProperty</a>
 

 

