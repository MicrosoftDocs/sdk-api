---
UID: NF:msrdc.IRdcGeneratorFilterMaxParameters.SetHorizonSize
title: IRdcGeneratorFilterMaxParameters::SetHorizonSize (msrdc.h)
description: Sets the horizon size — the length over which the FilterMax generator looks for local maxima.
helpviewer_keywords: ["IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression]","SetHorizonSize method","IRdcGeneratorFilterMaxParameters.SetHorizonSize","IRdcGeneratorFilterMaxParameters::SetHorizonSize","SetHorizonSize","SetHorizonSize method [Remote Differential Compression]","SetHorizonSize method [Remote Differential Compression]","IRdcGeneratorFilterMaxParameters interface","fs.irdcgeneratorfiltermaxparameters_sethorizonsize","msrdc/IRdcGeneratorFilterMaxParameters::SetHorizonSize","rdc.irdcgeneratorfiltermaxparameters_sethorizonsize"]
old-location: rdc\irdcgeneratorfiltermaxparameters_sethorizonsize.htm
tech.root: rdc
ms.assetid: becd1edd-d06d-4328-8a7a-678f893bad3a
ms.date: 12/05/2018
ms.keywords: IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression],SetHorizonSize method, IRdcGeneratorFilterMaxParameters.SetHorizonSize, IRdcGeneratorFilterMaxParameters::SetHorizonSize, SetHorizonSize, SetHorizonSize method [Remote Differential Compression], SetHorizonSize method [Remote Differential Compression],IRdcGeneratorFilterMaxParameters interface, fs.irdcgeneratorfiltermaxparameters_sethorizonsize, msrdc/IRdcGeneratorFilterMaxParameters::SetHorizonSize, rdc.irdcgeneratorfiltermaxparameters_sethorizonsize
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
 - IRdcGeneratorFilterMaxParameters::SetHorizonSize
 - msrdc/IRdcGeneratorFilterMaxParameters::SetHorizonSize
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
 - IRdcGeneratorFilterMaxParameters.SetHorizonSize
---

# IRdcGeneratorFilterMaxParameters::SetHorizonSize


## -description

The <b>SetHorizonSize</b> 
    method sets the horizon size—the length over which the FilterMax generator looks 
    for local maxima. This determines the default smallest size for a chunk.

## -parameters

### -param horizonSize [in]

Specifies the length in bytes of the horizon size. 
      The valid range is from <b>MSRDC_MINIMUM_HORIZONSIZE</b> to 
      <b>MSRDC_MAXIMUM_HORIZONSIZE</b>. If this parameter is not set then a suitable default will 
      be used.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-gethorizonsize">GetHorizonSize</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorfiltermaxparameters">IRdcGeneratorFilterMaxParameters</a>
