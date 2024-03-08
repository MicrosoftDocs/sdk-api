---
UID: NS:medparam._MP_PARAMINFO
title: MP_PARAMINFO (medparam.h)
description: The MP_PARAMINFO structure contains information about a parameter.
helpviewer_keywords: ["MP_PARAMINFO","MP_PARAMINFO structure [DirectShow]","MP_PARAMINFOStructure","dshow.mp_paraminfo","medparam/MP_PARAMINFO"]
old-location: dshow\mp_paraminfo.htm
tech.root: dshow
ms.assetid: 91d2d08b-a55e-492f-a509-9c080cc438df
ms.date: 4/26/2023
ms.keywords: MP_PARAMINFO, MP_PARAMINFO structure [DirectShow], MP_PARAMINFOStructure, dshow.mp_paraminfo, medparam/MP_PARAMINFO
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MP_PARAMINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MP_PARAMINFO
 - medparam/_MP_PARAMINFO
 - MP_PARAMINFO
 - medparam/MP_PARAMINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Medparam.h
api_name:
 - MP_PARAMINFO
---

# MP_PARAMINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>MP_PARAMINFO</code> structure contains information about a parameter.

## -struct-fields

### -field mpType

Member of the <a href="/previous-versions/windows/desktop/api/medparam/ne-medparam-mp_type">MP_TYPE</a> enumeration that specifies the valid data type for this parameter.

### -field mopCaps

Bitwise combination of one or more <a href="/windows/desktop/DirectShow/parameter-capabilities-flags">Parameter Capabilities Flags</a> that specify which envelope curves are supported. For Boolean and enumeration parameters, only MP_CAPS_CURVE_JUMP is valid.

### -field mpdMinValue

Minimum value of the parameter. Used only for parameters with numeric values.

### -field mpdMaxValue

Maximum value of the parameter. Used only for parameters with numeric values.

### -field mpdNeutralValue

Default or "neutral" value of the parameter.

### -field szUnitText

NULL-terminated wide-character string that contains the name of the units for the parameter.

### -field szLabel

NULL-terminated wide-character string that contains the name of the parameter.

## -remarks

The <b>szUnitText</b> and <b>szLabel</b> members always contain English-language strings. For international support, use the <a href="/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getparamtext">IMediaParamInfo::GetParamText</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-structures">DMO Structures</a>