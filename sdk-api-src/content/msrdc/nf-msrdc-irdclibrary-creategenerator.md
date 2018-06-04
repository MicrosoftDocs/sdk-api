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

# IRdcLibrary::CreateGenerator


## -description


The <b>CreateGenerator</b> method
   creates a signature generator that will generate the specified levels of signatures.


## -parameters




### -param depth [in]

The number of levels of signatures to generate. The valid range is from 
    <b>MSRDC_MINIMUM_DEPTH</b> to <b>MSRDC_MAXIMUM_DEPTH</b>.


### -param iGeneratorParametersArray [in]

Pointer to an array of initialized 
    <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> interface pointers. Each 
    <b>IRdcGeneratorParameters</b> interface pointer would 
    have been initialized by 
    <a href="https://msdn.microsoft.com/a39e26bc-7493-4def-af6d-cf3620ec8a9f">IRdcLibrary::CreateGeneratorParameters</a> or 
    <a href="https://msdn.microsoft.com/c2ee5aea-c186-4017-bc35-2f83f5c05824">IRdcGenerator::GetGeneratorParameters</a>.


### -param iGenerator [out]

Pointer to a location that will receive the returned 
      <a href="https://msdn.microsoft.com/0288318a-0974-4870-b423-87c52090eb33">IRdcGenerator</a> interface pointer. Callers must release the 
      interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a39e26bc-7493-4def-af6d-cf3620ec8a9f">CreateGeneratorParameters</a>



<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>



<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>



<a href="https://msdn.microsoft.com/6fbced31-a230-44d4-a9ee-bb3e15df2563">OpenGeneratorParameters</a>
 

 

