---
UID: NF:msrdc.IRdcLibrary.CreateGeneratorParameters
title: IRdcLibrary::CreateGeneratorParameters (msrdc.h)
description: Returns an IRdcGeneratorParameters interface pointer initialized with the parameters necessary for a signature generator.
helpviewer_keywords: ["CreateGeneratorParameters","CreateGeneratorParameters method [Remote Differential Compression]","CreateGeneratorParameters method [Remote Differential Compression]","IRdcLibrary interface","IRdcLibrary interface [Remote Differential Compression]","CreateGeneratorParameters method","IRdcLibrary.CreateGeneratorParameters","IRdcLibrary::CreateGeneratorParameters","fs.irdclibrary_creategeneratorparameters","msrdc/IRdcLibrary::CreateGeneratorParameters","rdc.irdclibrary_creategeneratorparameters"]
old-location: rdc\irdclibrary_creategeneratorparameters.htm
tech.root: rdc
ms.assetid: a39e26bc-7493-4def-af6d-cf3620ec8a9f
ms.date: 12/05/2018
ms.keywords: CreateGeneratorParameters, CreateGeneratorParameters method [Remote Differential Compression], CreateGeneratorParameters method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],CreateGeneratorParameters method, IRdcLibrary.CreateGeneratorParameters, IRdcLibrary::CreateGeneratorParameters, fs.irdclibrary_creategeneratorparameters, msrdc/IRdcLibrary::CreateGeneratorParameters, rdc.irdclibrary_creategeneratorparameters
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
 - IRdcLibrary::CreateGeneratorParameters
 - msrdc/IRdcLibrary::CreateGeneratorParameters
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
 - IRdcLibrary.CreateGeneratorParameters
---

# IRdcLibrary::CreateGeneratorParameters


## -description

The 
    <b>CreateGeneratorParameters</b> method 
    returns an <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a> 
  interface pointer initialized with the  parameters necessary for a signature generator.

## -parameters

### -param parametersType [in]

Specifies the type of signature generator for the created parameters, enumerated by the 
    <a href="/windows/win32/api/msrdc/ne-msrdc-generatorparameterstype">GeneratorParametersType</a> enumeration. The initial 
  release of RDC only supports one type, <b>RDCGENTYPE_FilterMax</b>.

### -param level [in]

The recursion level for this parameter block. A parameter block is needed for each level of generated 
    signatures. The valid range is from <b>MSRDC_MINIMUM_DEPTH</b> to 
  <b>MSRDC_MAXIMUM_DEPTH</b>.

### -param iGeneratorParameters [out]

Pointer to a location that will receive an 
    <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a> interface pointer. On a 
  successful return the interface will be initialized on return. Callers must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/msrdc/ne-msrdc-generatorparameterstype">GeneratorParametersType</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdclibrary">IRdcLibrary</a>