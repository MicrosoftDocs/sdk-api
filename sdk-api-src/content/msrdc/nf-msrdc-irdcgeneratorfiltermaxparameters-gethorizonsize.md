---
UID: NF:msrdc.IRdcGeneratorFilterMaxParameters.GetHorizonSize
title: IRdcGeneratorFilterMaxParameters::GetHorizonSize (msrdc.h)
description: Returns the horizon size - the length over which the FilterMax generator looks for local maxima.
helpviewer_keywords: ["GetHorizonSize","GetHorizonSize method [Remote Differential Compression]","GetHorizonSize method [Remote Differential Compression]","IRdcGeneratorFilterMaxParameters interface","IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression]","GetHorizonSize method","IRdcGeneratorFilterMaxParameters.GetHorizonSize","IRdcGeneratorFilterMaxParameters::GetHorizonSize","fs.irdcgeneratorfiltermaxparameters_gethorizonsize","msrdc/IRdcGeneratorFilterMaxParameters::GetHorizonSize","rdc.irdcgeneratorfiltermaxparameters_gethorizonsize"]
old-location: rdc\irdcgeneratorfiltermaxparameters_gethorizonsize.htm
tech.root: rdc
ms.assetid: 6509330a-9592-4e10-91fb-43e4b63dceb9
ms.date: 12/05/2018
ms.keywords: GetHorizonSize, GetHorizonSize method [Remote Differential Compression], GetHorizonSize method [Remote Differential Compression],IRdcGeneratorFilterMaxParameters interface, IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression],GetHorizonSize method, IRdcGeneratorFilterMaxParameters.GetHorizonSize, IRdcGeneratorFilterMaxParameters::GetHorizonSize, fs.irdcgeneratorfiltermaxparameters_gethorizonsize, msrdc/IRdcGeneratorFilterMaxParameters::GetHorizonSize, rdc.irdcgeneratorfiltermaxparameters_gethorizonsize
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
 - IRdcGeneratorFilterMaxParameters::GetHorizonSize
 - msrdc/IRdcGeneratorFilterMaxParameters::GetHorizonSize
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
 - IRdcGeneratorFilterMaxParameters.GetHorizonSize
---

# IRdcGeneratorFilterMaxParameters::GetHorizonSize


## -description

The <b>GetHorizonSize</b> 
    method returns the horizon size—the length over which the FilterMax generator looks 
    for local maxima. This determines the default smallest size for a chunk.

## -parameters

### -param horizonSize [out]

Address of a <b>ULONG</b> that will receive the length in bytes of the horizon size. 
      The valid range is from <b>MSRDC_MINIMUM_HORIZONSIZE</b> to 
      <b>MSRDC_MAXIMUM_HORIZONSIZE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorfiltermaxparameters">IRdcGeneratorFilterMaxParameters</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-sethorizonsize">SetHorizonSize</a>
