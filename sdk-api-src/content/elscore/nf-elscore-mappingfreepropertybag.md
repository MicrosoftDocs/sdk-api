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

# MappingFreePropertyBag function


## -description


Frees memory and resources allocated during an ELS text recognition operation.


## -parameters




### -param pBag [in]

Pointer to a <a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a> structure containing the properties for which to free resources. This parameter cannot be set to <b>NULL</b>.


## -returns



Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.




## -remarks



An ELS service allocates memory and resources for data retrieved from application calls to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>. The <b>MappingFreePropertyBag</b> function releases these resources.

<div class="alert"><b>Caution</b>  Services should not be freed before freeing the property bags produced by those services.</div>
<div> </div>
<div class="alert"><b>Caution</b>  The application must call this function only once for each call to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a> when the property bag is no longer needed. Not calling <b>MappingFreePropertyBag</b> after each call to <b>MappingRecognizeText</b> causes a resource leak. For more information about memory allocation for the property bag, see the remarks for the <a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a> structure.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/90bc1757-ec94-425e-927f-9ae2e1ab8af8">Extended Linguistic Services</a>



<a href="https://msdn.microsoft.com/d62ab664-a75a-4d06-aefb-a3311ea7d4a7">Extended Linguistic Services Functions</a>



<a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a>



<a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>



<a href="https://msdn.microsoft.com/9db9045d-b289-4c6c-9b17-ddbc2c1d3089">Requesting Text Recognition</a>
 

 

