---
UID: NF:bdaiface.IBDA_AutoDemodulateEx.get_SupportedVideoFormats
title: IBDA_AutoDemodulateEx::get_SupportedVideoFormats (bdaiface.h)
description: The get_SupportedVideoFormats method retrieves the video formats that are supported by the demodulator.
helpviewer_keywords: ["IBDA_AutoDemodulateEx interface [Microsoft TV Technologies]","get_SupportedVideoFormats method","IBDA_AutoDemodulateEx.get_SupportedVideoFormats","IBDA_AutoDemodulateEx::get_SupportedVideoFormats","IBDA_AutoDemodulateExget_SupportedVideoFormats","bdaiface/IBDA_AutoDemodulateEx::get_SupportedVideoFormats","get_SupportedVideoFormats","get_SupportedVideoFormats method [Microsoft TV Technologies]","get_SupportedVideoFormats method [Microsoft TV Technologies]","IBDA_AutoDemodulateEx interface","mstv.ibda_autodemodulateex_get_supportedvideoformats"]
old-location: mstv\ibda_autodemodulateex_get_supportedvideoformats.htm
tech.root: mstv
ms.assetid: bba4a57c-7e07-45ca-84d0-921caf39f345
ms.date: 12/05/2018
ms.keywords: IBDA_AutoDemodulateEx interface [Microsoft TV Technologies],get_SupportedVideoFormats method, IBDA_AutoDemodulateEx.get_SupportedVideoFormats, IBDA_AutoDemodulateEx::get_SupportedVideoFormats, IBDA_AutoDemodulateExget_SupportedVideoFormats, bdaiface/IBDA_AutoDemodulateEx::get_SupportedVideoFormats, get_SupportedVideoFormats, get_SupportedVideoFormats method [Microsoft TV Technologies], get_SupportedVideoFormats method [Microsoft TV Technologies],IBDA_AutoDemodulateEx interface, mstv.ibda_autodemodulateex_get_supportedvideoformats
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - IBDA_AutoDemodulateEx::get_SupportedVideoFormats
 - bdaiface/IBDA_AutoDemodulateEx::get_SupportedVideoFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_AutoDemodulateEx.get_SupportedVideoFormats
---

# IBDA_AutoDemodulateEx::get_SupportedVideoFormats


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SupportedVideoFormats</b> method retrieves the video formats that are supported by the demodulator.

## -parameters

### -param pulAMTunerModeType [out]

Pointer to a variable that receives a mask that indicates the frequency ranges that are supported by the BDA device filter. For a list of valid mask bits, see <a href="/previous-versions/ms778981(v=vs.85)">AMTunerModeType Enumeration</a>.

### -param pulAnalogVideoStandard [out]

Pointer to a variable that receives a mask that indicates the analog television signal formats that are supported by the BDA device filter. For a list of valid mask bits, see <a href="/windows/win32/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard Enumeration</a>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_autodemodulateex">IBDA_AutoDemodulateEx Interface</a>