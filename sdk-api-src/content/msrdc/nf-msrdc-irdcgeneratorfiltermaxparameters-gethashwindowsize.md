---
UID: NF:msrdc.IRdcGeneratorFilterMaxParameters.GetHashWindowSize
title: IRdcGeneratorFilterMaxParameters::GetHashWindowSize (msrdc.h)
author: windows-sdk-content
description: Returns the hash window size&#8212;the size of the sliding window used by the FilterMax generator for computing the hash used in the local maxima calculations.
old-location: rdc\irdcgeneratorfiltermaxparameters_gethashwindowsize.htm
tech.root: rdc
ms.assetid: c1a0460c-ca48-48ca-bd5b-1213e8279366
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetHashWindowSize, GetHashWindowSize method [Remote Differential Compression], GetHashWindowSize method [Remote Differential Compression],IRdcGeneratorFilterMaxParameters interface, IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression],GetHashWindowSize method, IRdcGeneratorFilterMaxParameters.GetHashWindowSize, IRdcGeneratorFilterMaxParameters::GetHashWindowSize, fs.irdcgeneratorfiltermaxparameters_gethashwindowsize, msrdc/IRdcGeneratorFilterMaxParameters::GetHashWindowSize, rdc.irdcgeneratorfiltermaxparameters_gethashwindowsize
ms.topic: method
f1_keywords: 
 - "msrdc/IRdcGeneratorFilterMaxParameters.GetHashWindowSize"
dev_langs:
 - c++
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
 - IRdcGeneratorFilterMaxParameters.GetHashWindowSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRdcGeneratorFilterMaxParameters::GetHashWindowSize


## -description


The <b>GetHashWindowSize</b> 
    method returns the hash window size—the size of the sliding window used by the 
    FilterMax generator for computing the hash used in the local maxima calculations.


## -parameters




### -param hashWindowSize [out]

Address of a <b>ULONG</b> that will receive the length in bytes of the hash window 
      size. The valid range is from <b>MSRDC_MINIMUM_HASHWINDOWSIZE</b> to 
      <b>MSRDC_MAXIMUM_HASHWINDOWSIZE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorfiltermaxparameters">IRdcGeneratorFilterMaxParameters</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorfiltermaxparameters-sethashwindowsize">SetHashWindowSize</a>
 

 

