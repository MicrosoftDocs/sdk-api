---
UID: NF:strmif.IAMVideoDecimationProperties.SetDecimationUsage
title: IAMVideoDecimationProperties::SetDecimationUsage (strmif.h)
description: The SetDecimationUsage method sets the decimation strategy.
helpviewer_keywords: ["IAMVideoDecimationProperties interface [DirectShow]","SetDecimationUsage method","IAMVideoDecimationProperties.SetDecimationUsage","IAMVideoDecimationProperties::SetDecimationUsage","IAMVideoDecimationPropertiesSetDecimationUsage","SetDecimationUsage","SetDecimationUsage method [DirectShow]","SetDecimationUsage method [DirectShow]","IAMVideoDecimationProperties interface","dshow.iamvideodecimationproperties_setdecimationusage","strmif/IAMVideoDecimationProperties::SetDecimationUsage"]
old-location: dshow\iamvideodecimationproperties_setdecimationusage.htm
tech.root: dshow
ms.assetid: c6456154-48f5-41d9-b6f5-863b30a53596
ms.date: 12/05/2018
ms.keywords: IAMVideoDecimationProperties interface [DirectShow],SetDecimationUsage method, IAMVideoDecimationProperties.SetDecimationUsage, IAMVideoDecimationProperties::SetDecimationUsage, IAMVideoDecimationPropertiesSetDecimationUsage, SetDecimationUsage, SetDecimationUsage method [DirectShow], SetDecimationUsage method [DirectShow],IAMVideoDecimationProperties interface, dshow.iamvideodecimationproperties_setdecimationusage, strmif/IAMVideoDecimationProperties::SetDecimationUsage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVideoDecimationProperties::SetDecimationUsage
 - strmif/IAMVideoDecimationProperties::SetDecimationUsage
dev_langs:
 - c++
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
---

# IAMVideoDecimationProperties::SetDecimationUsage


## -description

The <code>SetDecimationUsage</code> method sets the decimation strategy.

## -parameters

### -param Usage [in]

Member of the [DECIMATION_USAGE](/windows/desktop/api/strmif/ne-strmif-decimation_usage) enumeration that specifies the decimation strategy.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_INVALIDARG otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideodecimationproperties">IAMVideoDecimationProperties Interface</a>