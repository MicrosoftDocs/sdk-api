---
UID: NF:msrdc.IRdcGeneratorParameters.GetGeneratorParametersType
title: IRdcGeneratorParameters::GetGeneratorParametersType (msrdc.h)
description: Returns the specific type of the parameters.
helpviewer_keywords: ["GetGeneratorParametersType","GetGeneratorParametersType method [Remote Differential Compression]","GetGeneratorParametersType method [Remote Differential Compression]","IRdcGeneratorParameters interface","IRdcGeneratorParameters interface [Remote Differential Compression]","GetGeneratorParametersType method","IRdcGeneratorParameters.GetGeneratorParametersType","IRdcGeneratorParameters::GetGeneratorParametersType","fs.irdcgeneratorparameters_getgeneratorparameterstype","msrdc/IRdcGeneratorParameters::GetGeneratorParametersType","rdc.irdcgeneratorparameters_getgeneratorparameterstype"]
old-location: rdc\irdcgeneratorparameters_getgeneratorparameterstype.htm
tech.root: rdc
ms.assetid: d9fd60d5-a542-4a00-becd-85c7dafbe105
ms.date: 12/05/2018
ms.keywords: GetGeneratorParametersType, GetGeneratorParametersType method [Remote Differential Compression], GetGeneratorParametersType method [Remote Differential Compression],IRdcGeneratorParameters interface, IRdcGeneratorParameters interface [Remote Differential Compression],GetGeneratorParametersType method, IRdcGeneratorParameters.GetGeneratorParametersType, IRdcGeneratorParameters::GetGeneratorParametersType, fs.irdcgeneratorparameters_getgeneratorparameterstype, msrdc/IRdcGeneratorParameters::GetGeneratorParametersType, rdc.irdcgeneratorparameters_getgeneratorparameterstype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcGeneratorParameters::GetGeneratorParametersType
 - msrdc/IRdcGeneratorParameters::GetGeneratorParametersType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcGeneratorParameters.GetGeneratorParametersType
---

# IRdcGeneratorParameters::GetGeneratorParametersType


## -description

The 
   <b>GetGeneratorParametersType</b> 
   method returns the specific type of the parameters.

## -parameters

### -param parametersType [out]

The address of a <a href="/windows/win32/api/msrdc/ne-msrdc-generatorparameterstype">GeneratorParametersType</a> that will receive the type of the parameters.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/msrdc/ne-msrdc-generatorparameterstype">GeneratorParametersType</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a>