---
UID: NF:vpconfig.IVPBaseConfig.GetVideoFormats
title: IVPBaseConfig::GetVideoFormats (vpconfig.h)
description: The GetVideoFormats method retrieves the video formats the driver supports.
helpviewer_keywords: ["GetVideoFormats","GetVideoFormats method [DirectShow]","GetVideoFormats method [DirectShow]","IVPBaseConfig interface","IVPBaseConfig interface [DirectShow]","GetVideoFormats method","IVPBaseConfig.GetVideoFormats","IVPBaseConfig::GetVideoFormats","IVPBaseConfigGetVideoFormats","dshow.ivpbaseconfig_getvideoformats","vpconfig/IVPBaseConfig::GetVideoFormats"]
old-location: dshow\ivpbaseconfig_getvideoformats.htm
tech.root: dshow
ms.assetid: a0426a2a-a856-4e5d-8ff2-4afa3b18355e
ms.date: 4/26/2023
ms.keywords: GetVideoFormats, GetVideoFormats method [DirectShow], GetVideoFormats method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetVideoFormats method, IVPBaseConfig.GetVideoFormats, IVPBaseConfig::GetVideoFormats, IVPBaseConfigGetVideoFormats, dshow.ivpbaseconfig_getvideoformats, vpconfig/IVPBaseConfig::GetVideoFormats
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
 - IVPBaseConfig::GetVideoFormats
 - vpconfig/IVPBaseConfig::GetVideoFormats
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
 - IVPBaseConfig.GetVideoFormats
---

# IVPBaseConfig::GetVideoFormats


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetVideoFormats</code> method retrieves the video formats the driver supports.

## -parameters

### -param pdwNumFormats [in, out]

Pointer to a variable that specifies the number of <b>DDPIXELFORMAT</b> structures in the <i>pddPixelFormats</i> array. On input, specifies the size of the array (in number of array elements). On output, contains the actual number of <b>DDPIXELFORMAT</b> structures that were copied into the array. If <i>pddPixelFormat</i> is <b>NULL</b>, the method returns the required array size.

### -param pddPixelFormats [in, out]

Pointer to an array of <b>DDPIXELFORMAT</b> structures, allocated by the caller. The device fills in the array with the format information.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -remarks

The client first calls this method with the value <b>NULL</b> for the <i>pddPixelFormats</i> parameter. The device returns the number of <b>DDPIXELFORMAT</b> structures in the <i>pddPixelFormatso</i> parameter. The client allocates an array of that size, and calls the method again, passing the address of the array in the <i>pddPixelFormats</i> parameter. The device copies the format information into the buffer, and returns the actual number of copied structures in the <i>pddPixelFormats</i> parameter.

The <b>DDPIXELFORMAT</b> structure is documented in the Windows DDK.

The client sets the format by calling the <a href="/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setvideoformat">IVPBaseConfig::SetVideoFormat</a> method with an index number, which references one of the format structures returned by this method.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>