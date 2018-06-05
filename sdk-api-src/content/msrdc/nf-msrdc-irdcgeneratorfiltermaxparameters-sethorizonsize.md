---
UID: NF:msrdc.IRdcGeneratorFilterMaxParameters.SetHorizonSize
title: IRdcGeneratorFilterMaxParameters::SetHorizonSize
author: windows-sdk-content
description: Sets the horizon size&#8212;the length over which the FilterMax generator looks for local maxima.
old-location: rdc\irdcgeneratorfiltermaxparameters_sethorizonsize.htm
old-project: Rdc
ms.assetid: becd1edd-d06d-4328-8a7a-678f893bad3a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRdcGeneratorFilterMaxParameters interface [Remote Differential Compression],SetHorizonSize method, IRdcGeneratorFilterMaxParameters.SetHorizonSize, IRdcGeneratorFilterMaxParameters::SetHorizonSize, SetHorizonSize, SetHorizonSize method [Remote Differential Compression], SetHorizonSize method [Remote Differential Compression],IRdcGeneratorFilterMaxParameters interface, fs.irdcgeneratorfiltermaxparameters_sethorizonsize, msrdc/IRdcGeneratorFilterMaxParameters::SetHorizonSize, rdc.irdcgeneratorfiltermaxparameters_sethorizonsize
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IRdcGeneratorFilterMaxParameters.SetHorizonSize
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6509330a-9592-4e10-91fb-43e4b63dceb9">GetHorizonSize</a>



<a href="https://msdn.microsoft.com/6767ab24-2bb6-48bf-8f12-794d8b22e2b7">IRdcGeneratorFilterMaxParameters</a>
 

 

