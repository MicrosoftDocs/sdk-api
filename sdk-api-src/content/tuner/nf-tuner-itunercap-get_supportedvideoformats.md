---
UID: NF:tuner.ITunerCap.get_SupportedVideoFormats
title: ITunerCap::get_SupportedVideoFormats (tuner.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["ITunerCap interface [Microsoft TV Technologies]","get_SupportedVideoFormats method","ITunerCap.get_SupportedVideoFormats","ITunerCap::get_SupportedVideoFormats","ITunerCapget_SupportedVideoFormats","get_SupportedVideoFormats","get_SupportedVideoFormats method [Microsoft TV Technologies]","get_SupportedVideoFormats method [Microsoft TV Technologies]","ITunerCap interface","mstv.itunercap_get_supportedvideoformats","tuner/ITunerCap::get_SupportedVideoFormats"]
old-location: mstv\itunercap_get_supportedvideoformats.htm
tech.root: mstv
ms.assetid: 301402bd-8c9c-4dab-a00b-29aaa8efb2a2
ms.date: 12/05/2018
ms.keywords: ITunerCap interface [Microsoft TV Technologies],get_SupportedVideoFormats method, ITunerCap.get_SupportedVideoFormats, ITunerCap::get_SupportedVideoFormats, ITunerCapget_SupportedVideoFormats, get_SupportedVideoFormats, get_SupportedVideoFormats method [Microsoft TV Technologies], get_SupportedVideoFormats method [Microsoft TV Technologies],ITunerCap interface, mstv.itunercap_get_supportedvideoformats, tuner/ITunerCap::get_SupportedVideoFormats
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - ITunerCap::get_SupportedVideoFormats
 - tuner/ITunerCap::get_SupportedVideoFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITunerCap.get_SupportedVideoFormats
---

# ITunerCap::get_SupportedVideoFormats


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_SupportedVideoFormats</b> method retrieves the video formats that are supported by the TV tuner.

## -parameters

### -param pulAMTunerModeType [out]

Receives a bitmask that indicates the frequency ranges that are supported by the BDA device filter. For a list of valid mask bits, see <a href="/previous-versions/ms778981(v=vs.85)">AMTunerModeType Enumeration</a>.

### -param pulAnalogVideoStandard [out]

Receives a bitmask that indicates the analog television signal formats that are supported by the BDA device filter. For a list of valid mask bits, see <a href="/windows/win32/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard Enumeration</a>.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunercap">ITunerCap Interface</a>