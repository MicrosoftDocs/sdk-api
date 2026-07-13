---
UID: NF:vpconfig.IVPBaseConfig.GetVPDataInfo
title: IVPBaseConfig::GetVPDataInfo (vpconfig.h)
description: The GetVPDataInfo method retrieves the current video port data information.
helpviewer_keywords: ["GetVPDataInfo","GetVPDataInfo method [DirectShow]","GetVPDataInfo method [DirectShow]","IVPBaseConfig interface","IVPBaseConfig interface [DirectShow]","GetVPDataInfo method","IVPBaseConfig.GetVPDataInfo","IVPBaseConfig::GetVPDataInfo","IVPBaseConfigGetVPDataInfo","dshow.ivpbaseconfig_getvpdatainfo","vpconfig/IVPBaseConfig::GetVPDataInfo"]
old-location: dshow\ivpbaseconfig_getvpdatainfo.htm
tech.root: dshow
ms.assetid: 385ab5e4-b904-4268-a97e-1c3e7789b0a2
ms.date: 4/26/2023
ms.keywords: GetVPDataInfo, GetVPDataInfo method [DirectShow], GetVPDataInfo method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetVPDataInfo method, IVPBaseConfig.GetVPDataInfo, IVPBaseConfig::GetVPDataInfo, IVPBaseConfigGetVPDataInfo, dshow.ivpbaseconfig_getvpdatainfo, vpconfig/IVPBaseConfig::GetVPDataInfo
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
 - IVPBaseConfig::GetVPDataInfo
 - vpconfig/IVPBaseConfig::GetVPDataInfo
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
 - IVPBaseConfig.GetVPDataInfo
---

# IVPBaseConfig::GetVPDataInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetVPDataInfo</code> method retrieves the current video port data information.

## -parameters

### -param pamvpDataInfo [in, out]

Pointer to an <a href="/previous-versions/windows/desktop/api/vptype/ns-vptype-amvpdatainfo">AMVPDATAINFO</a> structure allocated by the caller. The device fills in the structure with information about the video port.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>