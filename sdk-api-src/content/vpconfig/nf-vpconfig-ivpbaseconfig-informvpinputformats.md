---
UID: NF:vpconfig.IVPBaseConfig.InformVPInputFormats
title: IVPBaseConfig::InformVPInputFormats (vpconfig.h)
description: The InformVPInputFormats method informs the device what video formats the video port supports.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","InformVPInputFormats method","IVPBaseConfig.InformVPInputFormats","IVPBaseConfig::InformVPInputFormats","IVPBaseConfigInformVPInputFormats","InformVPInputFormats","InformVPInputFormats method [DirectShow]","InformVPInputFormats method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_informvpinputformats","vpconfig/IVPBaseConfig::InformVPInputFormats"]
old-location: dshow\ivpbaseconfig_informvpinputformats.htm
tech.root: dshow
ms.assetid: d9b4ea2b-ad71-4226-9aad-e68a9cb26274
ms.date: 4/26/2023
ms.keywords: IVPBaseConfig interface [DirectShow],InformVPInputFormats method, IVPBaseConfig.InformVPInputFormats, IVPBaseConfig::InformVPInputFormats, IVPBaseConfigInformVPInputFormats, InformVPInputFormats, InformVPInputFormats method [DirectShow], InformVPInputFormats method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_informvpinputformats, vpconfig/IVPBaseConfig::InformVPInputFormats
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
 - IVPBaseConfig::InformVPInputFormats
 - vpconfig/IVPBaseConfig::InformVPInputFormats
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
 - IVPBaseConfig.InformVPInputFormats
---

# IVPBaseConfig::InformVPInputFormats


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>InformVPInputFormats</code> method informs the device what video formats the video port supports.

## -parameters

### -param dwNumFormats [in]

Number of video formats contained in the <i>pDDPixelFormats</i> parameter.

### -param pDDPixelFormats [in]

Pointer to an array of pixel format structures (<b>DDPIXELFORMAT</b>) to send to the device.

## -returns

Returns S_FALSE if failure, or S_OK otherwise.

## -remarks

The supplied array of supported video port formats might determine what formats the device, in turn, proposes.

The <b>DDPIXELFORMAT</b> structure is documented in the Windows DDK.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>