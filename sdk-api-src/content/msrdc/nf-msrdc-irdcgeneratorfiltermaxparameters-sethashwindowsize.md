---
UID: NF:msrdc.IRdcGeneratorFilterMaxParameters.SetHashWindowSize
title: IRdcGeneratorFilterMaxParameters::SetHashWindowSize (msrdc.h)
description: Sets the hash window size - the size of the sliding window used by the FilterMax generator for computing the hash used in the local maxima calculations.
helpviewer_keywords: ["IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression]","SetHashWindowSize method","IRdcGeneratorFilterMaxParameters.SetHashWindowSize","IRdcGeneratorFilterMaxParameters::SetHashWindowSize","SetHashWindowSize","SetHashWindowSize method [Remote Differential Compression]","SetHashWindowSize method [Remote Differential Compression]","IRdcGeneratorFilterMaxParameters interface","fs.irdcgeneratorfiltermaxparameters_sethashwindowsize","msrdc/IRdcGeneratorFilterMaxParameters::SetHashWindowSize","rdc.irdcgeneratorfiltermaxparameters_sethashwindowsize"]
old-location: rdc\irdcgeneratorfiltermaxparameters_sethashwindowsize.htm
tech.root: rdc
ms.assetid: b18a5db1-f480-46c4-bac3-b0b2f0da6cfa
ms.date: 12/05/2018
ms.keywords: IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression],SetHashWindowSize method, IRdcGeneratorFilterMaxParameters.SetHashWindowSize, IRdcGeneratorFilterMaxParameters::SetHashWindowSize, SetHashWindowSize, SetHashWindowSize method [Remote Differential Compression], SetHashWindowSize method [Remote Differential Compression],IRdcGeneratorFilterMaxParameters interface, fs.irdcgeneratorfiltermaxparameters_sethashwindowsize, msrdc/IRdcGeneratorFilterMaxParameters::SetHashWindowSize, rdc.irdcgeneratorfiltermaxparameters_sethashwindowsize
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
 - IRdcGeneratorFilterMaxParameters::SetHashWindowSize
 - msrdc/IRdcGeneratorFilterMaxParameters::SetHashWindowSize
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
 - IRdcGeneratorFilterMaxParameters.SetHashWindowSize
---

# IRdcGeneratorFilterMaxParameters::SetHashWindowSize


## -description

The <b>SetHashWindowSize</b> 
    method sets the hash window size—the size of the sliding window used by the 
    FilterMax generator for computing the hash used in the local maxima calculations.

## -parameters

### -param hashWindowSize [in]

The length in bytes of the hash window size. The valid range is from 
      <b>MSRDC_MINIMUM_HASHWINDOWSIZE</b> to 
      <b>MSRDC_MAXIMUM_HASHWINDOWSIZE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-gethashwindowsize">GetHashWindowSize</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorfiltermaxparameters">IRdcGeneratorFilterMaxParameters</a>
