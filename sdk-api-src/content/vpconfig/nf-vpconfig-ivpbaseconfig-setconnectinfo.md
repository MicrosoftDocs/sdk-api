---
UID: NF:vpconfig.IVPBaseConfig.SetConnectInfo
title: IVPBaseConfig::SetConnectInfo (vpconfig.h)
description: The SetConnectInfo method sets the video port connection parameters.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","SetConnectInfo method","IVPBaseConfig.SetConnectInfo","IVPBaseConfig::SetConnectInfo","IVPBaseConfigSetConnectInfo","SetConnectInfo","SetConnectInfo method [DirectShow]","SetConnectInfo method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_setconnectinfo","vpconfig/IVPBaseConfig::SetConnectInfo"]
old-location: dshow\ivpbaseconfig_setconnectinfo.htm
tech.root: dshow
ms.assetid: e52bb213-e6e7-4bae-9e1e-6b34f34cf1d1
ms.date: 4/26/2023
ms.keywords: IVPBaseConfig interface [DirectShow],SetConnectInfo method, IVPBaseConfig.SetConnectInfo, IVPBaseConfig::SetConnectInfo, IVPBaseConfigSetConnectInfo, SetConnectInfo, SetConnectInfo method [DirectShow], SetConnectInfo method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setconnectinfo, vpconfig/IVPBaseConfig::SetConnectInfo
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
 - IVPBaseConfig::SetConnectInfo
 - vpconfig/IVPBaseConfig::SetConnectInfo
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
 - IVPBaseConfig.SetConnectInfo
---

# IVPBaseConfig::SetConnectInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetConnectInfo</code> method sets the video port connection parameters.

## -parameters

### -param dwChosenEntry [in]

Specifies the index of connect information to pass to the driver. The value is a zero-based index into the array returned by the <a href="/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getconnectinfo">IVPBaseConfig::GetConnectInfo</a> method.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>