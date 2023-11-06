---
UID: NS:dxva9typ._DXVA_COPPSetSignalingCmdData
title: DXVA_COPPSetSignalingCmdData (dxva9typ.h)
description: Contains information for the Set Signal command in Certified Output Protection Protocol (COPP).
helpviewer_keywords: ["DXVA_COPPSetSignalingCmdData","DXVA_COPPSetSignalingCmdData structure [DirectShow]","DXVA_COPPSetSignalingCmdDataStructure","_DXVA_COPPSetSignalingCmdData","dshow.dxva_coppsetsignalingcmddata","dxva9typ/DXVA_COPPSetSignalingCmdData"]
old-location: dshow\dxva_coppsetsignalingcmddata.htm
tech.root: dshow
ms.assetid: f104b0c6-2b2f-4e6a-97e6-d73008cb80ef
ms.date: 4/26/2023
ms.keywords: DXVA_COPPSetSignalingCmdData, DXVA_COPPSetSignalingCmdData structure [DirectShow], DXVA_COPPSetSignalingCmdDataStructure, _DXVA_COPPSetSignalingCmdData, dshow.dxva_coppsetsignalingcmddata, dxva9typ/DXVA_COPPSetSignalingCmdData
req.header: dxva9typ.h
req.include-header: Dxva.h
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
req.typenames: DXVA_COPPSetSignalingCmdData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA_COPPSetSignalingCmdData
 - dxva9typ/_DXVA_COPPSetSignalingCmdData
 - DXVA_COPPSetSignalingCmdData
 - dxva9typ/DXVA_COPPSetSignalingCmdData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - DXVA_COPPSetSignalingCmdData
---

# DXVA_COPPSetSignalingCmdData structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains information for the Set Signal command in Certified Output Protection Protocol (COPP).

This command causes the driver to insert Wide Screen Signalling (WSS) codes or other data packets in the television signal, as required by some Analog Copy Protection (ACP) and Copy Generation Management System — Analog (CGMS-A) specifications. For example:
<ul>
<li>ETSI EN 300 294 (625i PAL): Data packets are inserted into line 23 of the signal.</li>
<li>CEA-608-B (NTSC): Data packets are inserted into line 21 of the vertical blanking interval (VBI).</li>
</ul>

## -struct-fields

### -field ActiveTVProtectionStandard

Specifies the protection standard and format that is current active. The value is a member of the <a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_tvprotectionstandard">COPP_TVProtectionStandard</a> enumeration.

### -field AspectRatioChangeMask1

Bit mask indicating which bits from <b>AspectRatioData1</b> to set in the signal.

### -field AspectRatioData1

Specifies the aspect ratio value to be set for the current protection standard. For EN 300 294, use the <a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_imageaspectratio_en300294">COPP_ImageAspectRatio_EN300294</a> enumeration.

### -field AspectRatioChangeMask2

Bit mask indicating which bits from <b>AspectRatioData2</b> to set in the signal.

### -field AspectRatioData2

An additional data element related to aspect ratio. The presence and meaning of this data depends on the protection standard. This field can be used to convey End and Q0 bits for EIA-608-B, or the active format description for CEA-805-A.

### -field AspectRatioChangeMask3

Bit mask indicating which bits from <b>AspectRatioData3</b> to set in the signal.

### -field AspectRatioData3

An additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard.

### -field ExtendedInfoChangeMask

Array of bit masks indicating which bits in <b>ExtendedInfoData</b> to change. This array is currently not used. Set each member to zero.

### -field ExtendedInfoData

Additional signaling elements to be set. This array is currently not used.
          Set each member to zero.

### -field Reserved

Reserved. Set to zero.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>