---
UID: NF:msrdc.IRdcGeneratorFilterMaxParameters.GetHorizonSize
title: IRdcGeneratorFilterMaxParameters::GetHorizonSize
author: windows-driver-content
description: Returns the horizon size&#8212;the length over which the FilterMax generator looks for local maxima.
old-location: rdc\irdcgeneratorfiltermaxparameters_gethorizonsize.htm
old-project: Rdc
ms.assetid: 6509330a-9592-4e10-91fb-43e4b63dceb9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetHorizonSize, GetHorizonSize method [Remote Differential Compression], GetHorizonSize method [Remote Differential Compression],IRdcGeneratorFilterMaxParameters interface, IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression],GetHorizonSize method, IRdcGeneratorFilterMaxParameters.GetHorizonSize, IRdcGeneratorFilterMaxParameters::GetHorizonSize, fs.irdcgeneratorfiltermaxparameters_gethorizonsize, msrdc/IRdcGeneratorFilterMaxParameters::GetHorizonSize, rdc.irdcgeneratorfiltermaxparameters_gethorizonsize
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
-	IRdcGeneratorFilterMaxParameters.GetHorizonSize
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6767ab24-2bb6-48bf-8f12-794d8b22e2b7">IRdcGeneratorFilterMaxParameters</a>



<a href="https://msdn.microsoft.com/becd1edd-d06d-4328-8a7a-678f893bad3a">SetHorizonSize</a>
 

 

