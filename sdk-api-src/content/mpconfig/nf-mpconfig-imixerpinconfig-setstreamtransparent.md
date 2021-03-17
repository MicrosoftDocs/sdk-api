---
UID: NF:mpconfig.IMixerPinConfig.SetStreamTransparent
title: IMixerPinConfig::SetStreamTransparent (mpconfig.h)
description: The SetStreamTransparent method sets the stream to transparent.
helpviewer_keywords: ["IMixerPinConfig interface [DirectShow]","SetStreamTransparent method","IMixerPinConfig.SetStreamTransparent","IMixerPinConfig::SetStreamTransparent","IMixerPinConfigSetStreamTransparent","SetStreamTransparent","SetStreamTransparent method [DirectShow]","SetStreamTransparent method [DirectShow]","IMixerPinConfig interface","dshow.imixerpinconfig_setstreamtransparent","mpconfig/IMixerPinConfig::SetStreamTransparent"]
old-location: dshow\imixerpinconfig_setstreamtransparent.htm
tech.root: dshow
ms.assetid: d1f60a35-ffef-4ebb-b331-558772310bcb
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetStreamTransparent method, IMixerPinConfig.SetStreamTransparent, IMixerPinConfig::SetStreamTransparent, IMixerPinConfigSetStreamTransparent, SetStreamTransparent, SetStreamTransparent method [DirectShow], SetStreamTransparent method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setstreamtransparent, mpconfig/IMixerPinConfig::SetStreamTransparent
req.header: mpconfig.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMixerPinConfig::SetStreamTransparent
 - mpconfig/IMixerPinConfig::SetStreamTransparent
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
 - IMixerPinConfig.SetStreamTransparent
---

# IMixerPinConfig::SetStreamTransparent


## -description

The <code>SetStreamTransparent</code> method sets the stream to transparent.

## -parameters

### -param bStreamTransparent [in]

Value specifying the transparency of the stream. Pass in <b>TRUE</b> to indicate stream is transparent; <b>FALSE</b> to indicate not a transparent stream.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getstreamtransparent">IMixerPinConfig::GetStreamTransparent</a>