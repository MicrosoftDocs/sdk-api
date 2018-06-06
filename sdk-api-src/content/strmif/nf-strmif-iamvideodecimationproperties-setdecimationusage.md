---
UID: NF:strmif.IAMVideoDecimationProperties.SetDecimationUsage
title: IAMVideoDecimationProperties::SetDecimationUsage
author: windows-sdk-content
description: The SetDecimationUsage method sets the decimation strategy.
old-location: dshow\iamvideodecimationproperties_setdecimationusage.htm
old-project: DirectShow
ms.assetid: c6456154-48f5-41d9-b6f5-863b30a53596
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMVideoDecimationProperties interface [DirectShow],SetDecimationUsage method, IAMVideoDecimationProperties.SetDecimationUsage, IAMVideoDecimationProperties::SetDecimationUsage, IAMVideoDecimationPropertiesSetDecimationUsage, SetDecimationUsage, SetDecimationUsage method [DirectShow], SetDecimationUsage method [DirectShow],IAMVideoDecimationProperties interface, dshow.iamvideodecimationproperties_setdecimationusage, strmif/IAMVideoDecimationProperties::SetDecimationUsage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoDecimationProperties.SetDecimationUsage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoDecimationProperties::SetDecimationUsage


## -description



The <code>SetDecimationUsage</code> method sets the decimation strategy.




## -parameters




### -param Usage [in]

Member of the <a href="https://msdn.microsoft.com/4c39f7f9-2d9c-4db5-9a2b-cf221ddedf80">DECIMATION_USAGE</a> enumeration that specifies the decimation strategy.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_INVALIDARG otherwise.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fd435eff-a4bc-40b3-8aa7-50d78d17e4ce">IAMVideoDecimationProperties Interface</a>
 

 

