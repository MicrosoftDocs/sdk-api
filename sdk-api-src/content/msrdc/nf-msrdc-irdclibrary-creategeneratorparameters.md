---
UID: NF:msrdc.IRdcLibrary.CreateGeneratorParameters
title: IRdcLibrary::CreateGeneratorParameters method
author: windows-driver-content
description: Returns an IRdcGeneratorParameters interface pointer initialized with the parameters necessary for a signature generator.
old-location: rdc\irdclibrary_creategeneratorparameters.htm
old-project: Rdc
ms.assetid: a39e26bc-7493-4def-af6d-cf3620ec8a9f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateGeneratorParameters method [Remote Differential Compression], CreateGeneratorParameters method [Remote Differential Compression], IRdcLibrary interface, CreateGeneratorParameters,IRdcLibrary.CreateGeneratorParameters, IRdcLibrary, IRdcLibrary interface [Remote Differential Compression], CreateGeneratorParameters method, IRdcLibrary::CreateGeneratorParameters, fs.irdclibrary_creategeneratorparameters, msrdc/IRdcLibrary::CreateGeneratorParameters, rdc.irdclibrary_creategeneratorparameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsRdc.dll
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IRdcLibrary.CreateGeneratorParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRdcLibrary::CreateGeneratorParameters method


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
 

 

