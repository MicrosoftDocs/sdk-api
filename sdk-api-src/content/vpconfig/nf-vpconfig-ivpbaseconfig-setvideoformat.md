---
UID: NF:vpconfig.IVPBaseConfig.SetVideoFormat
title: IVPBaseConfig::SetVideoFormat (vpconfig.h)
description: The SetVideoFormat method sets the video format.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","SetVideoFormat method","IVPBaseConfig.SetVideoFormat","IVPBaseConfig::SetVideoFormat","IVPBaseConfigSetVideoFormat","SetVideoFormat","SetVideoFormat method [DirectShow]","SetVideoFormat method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_setvideoformat","vpconfig/IVPBaseConfig::SetVideoFormat"]
old-location: dshow\ivpbaseconfig_setvideoformat.htm
tech.root: dshow
ms.assetid: 98b4182f-c286-4f4a-86b8-40d093456628
ms.date: 12/05/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetVideoFormat method, IVPBaseConfig.SetVideoFormat, IVPBaseConfig::SetVideoFormat, IVPBaseConfigSetVideoFormat, SetVideoFormat, SetVideoFormat method [DirectShow], SetVideoFormat method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setvideoformat, vpconfig/IVPBaseConfig::SetVideoFormat
req.header: vpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPBaseConfig::SetVideoFormat
 - vpconfig/IVPBaseConfig::SetVideoFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetVideoFormat
---

# IVPBaseConfig::SetVideoFormat


## -description

The <code>SetVideoFormat</code> method sets the video format.

## -parameters

### -param dwChosenEntry [in]

Value specifying the index (zero-based) of the video pixel format to use.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Retrieve the video formats by using <a href="/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getvideoformats">IVPBaseConfig::GetVideoFormats</a>.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>