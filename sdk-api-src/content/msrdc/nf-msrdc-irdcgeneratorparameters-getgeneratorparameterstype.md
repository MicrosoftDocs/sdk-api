---
UID: NF:msrdc.IRdcGeneratorParameters.GetGeneratorParametersType
title: IRdcGeneratorParameters::GetGeneratorParametersType (msrdc.h)
author: windows-sdk-content
description: Returns the specific type of the parameters.
old-location: rdc\irdcgeneratorparameters_getgeneratorparameterstype.htm
tech.root: rdc
ms.assetid: d9fd60d5-a542-4a00-becd-85c7dafbe105
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGeneratorParametersType, GetGeneratorParametersType method [Remote Differential Compression], GetGeneratorParametersType method [Remote Differential Compression],IRdcGeneratorParameters interface, IRdcGeneratorParameters interface [Remote Differential Compression],GetGeneratorParametersType method, IRdcGeneratorParameters.GetGeneratorParametersType, IRdcGeneratorParameters::GetGeneratorParametersType, fs.irdcgeneratorparameters_getgeneratorparameterstype, msrdc/IRdcGeneratorParameters::GetGeneratorParametersType, rdc.irdcgeneratorparameters_getgeneratorparameterstype
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcGeneratorParameters.GetGeneratorParametersType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRdcGeneratorParameters::GetGeneratorParametersType


## -description


The 
   <b>GetGeneratorParametersType</b> 
   method returns the specific type of the parameters.


## -parameters




### -param parametersType [out]

The address of a <a href="https://msdn.microsoft.com/55abafd5-4c55-498c-a567-a64d9bb76856">GeneratorParametersType</a> that will receive the type of the parameters.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/55abafd5-4c55-498c-a567-a64d9bb76856">GeneratorParametersType</a>



<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>
 

 

