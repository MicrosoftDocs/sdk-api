---
UID: NE:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0002
title: GeneratorParametersType (msrdc.h)
description: Defines the set of supported generator parameters.
helpviewer_keywords: ["GeneratorParametersType","GeneratorParametersType enumeration [Remote Differential Compression]","RDCGENTYPE_FilterMax","RDCGENTYPE_Unused","fs.generatorparameterstype","msrdc/GeneratorParametersType","msrdc/RDCGENTYPE_FilterMax","msrdc/RDCGENTYPE_Unused","rdc.generatorparameterstype"]
old-location: rdc\generatorparameterstype.htm
tech.root: rdc
ms.assetid: 55abafd5-4c55-498c-a567-a64d9bb76856
ms.date: 12/05/2018
ms.keywords: GeneratorParametersType, GeneratorParametersType enumeration [Remote Differential Compression], RDCGENTYPE_FilterMax, RDCGENTYPE_Unused, fs.generatorparameterstype, msrdc/GeneratorParametersType, msrdc/RDCGENTYPE_FilterMax, msrdc/RDCGENTYPE_Unused, rdc.generatorparameterstype
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
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GeneratorParametersType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0002
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0002
 - GeneratorParametersType
 - msrdc/GeneratorParametersType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - GeneratorParametersType
---

# GeneratorParametersType enumeration


## -description

The <b>GeneratorParametersType</b> enumeration type 
    defines the set of supported generator parameters.

## -enum-fields

### -field RDCGENTYPE_Unused:0

The generator parameters type is unknown.

### -field RDCGENTYPE_FilterMax

The FilterMax generator was used to generate the parameters.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorfiltermaxparameters">IRdcGeneratorFilterMaxParameters</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-getgeneratorparameterstype">IRdcGeneratorParameters::GetGeneratorParametersType</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-creategeneratorparameters">IRdcLibrary::CreateGeneratorParameters</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-enumerations">Remote Differential Compression Enumerations</a>
