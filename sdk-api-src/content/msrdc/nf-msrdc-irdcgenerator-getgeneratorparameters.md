---
UID: NF:msrdc.IRdcGenerator.GetGeneratorParameters
title: IRdcGenerator::GetGeneratorParameters
author: windows-sdk-content
description: Returns a copy of the parameters used to create the generator.
old-location: rdc\irdcgenerator_getgeneratorparameters.htm
old-project: Rdc
ms.assetid: c2ee5aea-c186-4017-bc35-2f83f5c05824
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetGeneratorParameters, GetGeneratorParameters method [Remote Differential Compression], GetGeneratorParameters method [Remote Differential Compression],IRdcGenerator interface, IRdcGenerator interface [Remote Differential Compression],GetGeneratorParameters method, IRdcGenerator.GetGeneratorParameters, IRdcGenerator::GetGeneratorParameters, fs.irdcgenerator_getgeneratorparameters, msrdc/IRdcGenerator::GetGeneratorParameters, rdc.irdcgenerator_getgeneratorparameters
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcGenerator.GetGeneratorParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRdcGenerator::GetGeneratorParameters


## -description


The <b>GetGeneratorParameters</b> method 
    returns a copy of the parameters used to create the generator. The generator parameters are 
    fixed when the generator is created.


## -parameters




### -param level [in]

The generator level for the parameters to be returned. The range is 
      <b>MSRDC_MINIMUM_DEPTH</b> to <b>MSRDC_MAXIMUM_DEPTH</b>.


### -param iGeneratorParameters [out]

Address of a pointer that on successful return will contain the 
      <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> interface pointer for the 
      parameters for the generator level specified in the <i>level</i> parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0288318a-0974-4870-b423-87c52090eb33">IRdcGenerator</a>



<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>
 

 

