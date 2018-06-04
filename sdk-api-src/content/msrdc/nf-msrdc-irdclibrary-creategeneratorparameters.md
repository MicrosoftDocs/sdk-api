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

# IRdcLibrary::CreateGeneratorParameters


## -description


The 
    <b>CreateGeneratorParameters</b> method 
    returns an <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> 
  interface pointer initialized with the  parameters necessary for a signature generator.


## -parameters




### -param parametersType [in]

Specifies the type of signature generator for the created parameters, enumerated by the 
    <a href="https://msdn.microsoft.com/55abafd5-4c55-498c-a567-a64d9bb76856">GeneratorParametersType</a> enumeration. The initial 
  release of RDC only supports one type, <b>RDCGENTYPE_FilterMax</b>.


### -param level [in]

The recursion level for this parameter block. A parameter block is needed for each level of generated 
    signatures. The valid range is from <b>MSRDC_MINIMUM_DEPTH</b> to 
  <b>MSRDC_MAXIMUM_DEPTH</b>.


### -param iGeneratorParameters [out]

Pointer to a location that will receive an 
    <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> interface pointer. On a 
  successful return the interface will be initialized on return. Callers must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/55abafd5-4c55-498c-a567-a64d9bb76856">GeneratorParametersType</a>



<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>



<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>
 

 

