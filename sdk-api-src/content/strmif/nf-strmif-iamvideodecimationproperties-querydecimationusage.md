---
UID: NF:strmif.IAMVideoDecimationProperties.QueryDecimationUsage
title: IAMVideoDecimationProperties::QueryDecimationUsage (strmif.h)
author: windows-sdk-content
description: The QueryDecimationUsage method retrieves the current decimation strategy.
old-location: dshow\iamvideodecimationproperties_querydecimationusage.htm
tech.root: DirectShow
ms.assetid: 3addb9be-61df-4310-9066-85f75c64aae4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMVideoDecimationProperties interface [DirectShow],QueryDecimationUsage method, IAMVideoDecimationProperties.QueryDecimationUsage, IAMVideoDecimationProperties::QueryDecimationUsage, IAMVideoDecimationPropertiesQueryDecimationUsage, QueryDecimationUsage, QueryDecimationUsage method [DirectShow], QueryDecimationUsage method [DirectShow],IAMVideoDecimationProperties interface, dshow.iamvideodecimationproperties_querydecimationusage, strmif/IAMVideoDecimationProperties::QueryDecimationUsage
ms.topic: method
f1_keywords: 
 - "strmif/IAMVideoDecimationProperties.QueryDecimationUsage"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoDecimationProperties.QueryDecimationUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoDecimationProperties::QueryDecimationUsage


## -description



The <code>QueryDecimationUsage</code> method retrieves the current decimation strategy.




## -parameters




### -param lpUsage [out]

Pointer to a variable of type <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_decimation_usage">DECIMATION_USAGE</a> that receives the decimation setting.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_FAIL or another error code otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideodecimationproperties">IAMVideoDecimationProperties Interface</a>
 

 

