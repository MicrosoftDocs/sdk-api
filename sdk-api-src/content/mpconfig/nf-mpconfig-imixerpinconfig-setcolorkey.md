---
UID: NF:mpconfig.IMixerPinConfig.SetColorKey
title: IMixerPinConfig::SetColorKey (mpconfig.h)
description: The SetColorKey method sets the color key being used by a video stream.
helpviewer_keywords: ["IMixerPinConfig interface [DirectShow]","SetColorKey method","IMixerPinConfig.SetColorKey","IMixerPinConfig::SetColorKey","IMixerPinConfigSetColorKey","SetColorKey","SetColorKey method [DirectShow]","SetColorKey method [DirectShow]","IMixerPinConfig interface","dshow.imixerpinconfig_setcolorkey","mpconfig/IMixerPinConfig::SetColorKey"]
old-location: dshow\imixerpinconfig_setcolorkey.htm
tech.root: dshow
ms.assetid: b2d4ffa2-0b10-4bc5-9af1-83f4ee68b35f
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetColorKey method, IMixerPinConfig.SetColorKey, IMixerPinConfig::SetColorKey, IMixerPinConfigSetColorKey, SetColorKey, SetColorKey method [DirectShow], SetColorKey method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setcolorkey, mpconfig/IMixerPinConfig::SetColorKey
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
 - IMixerPinConfig::SetColorKey
 - mpconfig/IMixerPinConfig::SetColorKey
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
 - IMixerPinConfig.SetColorKey
---

# IMixerPinConfig::SetColorKey


## -description

The <code>SetColorKey</code> method sets the color key being used by a video stream.

## -parameters

### -param pColorKey [in]

Pointer to a [COLORKEY](../strmif/ns-strmif-colorkey.md) structure.

## -returns

Returns an <code>HRESULT</code> value.

## -remarks

The term <i>color key</i> has different meanings depending on which stream it is referring to. The color key of the primary stream refers to the destination color key being used by the overlay surface. The color key of the secondary stream refers to the source color key used, when blitting from an offscreen surface to the primary surface.

Applications should set the color key of the primary pin to an obscure color (some color which, in all probability, will not be present on the desktop). Overlay mixer filters will try to pick an obscure color, but if the application knows that the specified color is part of some other content, then the application should change it.

Setting the color key on the secondary stream can be used to make the stream transparent and enable nonrectangular images. For example, if the secondary stream is closed-captioned text, then the closed-captioned text decoder should paint a solid color in the background and then set the color key on the corresponding pin to that color. This ensures that all pixels are transferred except those specified by the color key. If possible, applications should set the color key of the secondary stream to the same as that of the primary stream to give a slight performance advantage.

Setting this value on the primary stream sets the destination color key being used by the overlay surface. By default, the destination color key is used as the color key for all transparent (secondary) streams.

Valid arguments for the <i>pColorKey</i> parameter include CK_INDEX when video display mode is set to 256 colors, and CK_RGB when video display mode is set to a higher color depth such as hi-color, 24-bit, or 32-bit. The CK_RGB flag must be specified along with the CK_INDEX. If CK_INDEX flag is set then the index will be used as palette index in 256 color mode. But you must provide a <b>COLORREF</b> with a valid true color so that if the display mode is changed on the fly, DirectShow can switch to using the specified true color. This is because a number of true colors can be mapped to a single palette index, but going the other way from the palette index to a true color is not one-to-one.

<div class="alert"><b>Note</b>  Currently, this method is implemented only for the primary input pin.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getcolorkey">IMixerPinConfig::GetColorKey</a>