---
UID: NS:dxva9typ._DXVA_COPPSetProtectionLevelCmdData
title: DXVA_COPPSetProtectionLevelCmdData (dxva9typ.h)
description: Contains data for the Set Protection Level command in Certified Output Protection Protocol (COPP).
helpviewer_keywords: ["DXVA_COPPSetProtectionLevelCmdData","DXVA_COPPSetProtectionLevelCmdData structure [DirectShow]","DXVA_COPPSetProtectionLevelCmdDataStructure","_DXVA_COPPSetProtectionLevelCmdData","dshow.dxva_coppsetprotectionlevelcmddata","dxva9typ/DXVA_COPPSetProtectionLevelCmdData"]
old-location: dshow\dxva_coppsetprotectionlevelcmddata.htm
tech.root: dshow
ms.assetid: 19810f8f-2d23-4b01-864d-86ac82d40fe0
ms.date: 4/26/2023
ms.keywords: DXVA_COPPSetProtectionLevelCmdData, DXVA_COPPSetProtectionLevelCmdData structure [DirectShow], DXVA_COPPSetProtectionLevelCmdDataStructure, _DXVA_COPPSetProtectionLevelCmdData, dshow.dxva_coppsetprotectionlevelcmddata, dxva9typ/DXVA_COPPSetProtectionLevelCmdData
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
req.typenames: DXVA_COPPSetProtectionLevelCmdData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA_COPPSetProtectionLevelCmdData
 - dxva9typ/_DXVA_COPPSetProtectionLevelCmdData
 - DXVA_COPPSetProtectionLevelCmdData
 - dxva9typ/DXVA_COPPSetProtectionLevelCmdData
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
 - DXVA_COPPSetProtectionLevelCmdData
---

# DXVA_COPPSetProtectionLevelCmdData structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains data for the Set Protection Level command in Certified Output Protection Protocol (COPP).

## -struct-fields

### -field ProtType

Identifies the protection mechanism. See <a href="/windows/desktop/DirectShow/copp-protection-type-flags">COPP Protection Type Flags</a>.

### -field ProtLevel

Specifies the protection level. The meaning of this value depends on the protection mechanism that is queried. For each protection mechanism, the value of the <code>ProtLevel</code> member is a flag from a different enumeration, as shown in the following table.

<table>
<tr>
<th>Protection mechanism</th>
<th>Enumeration</th>
</tr>
<tr>
<td>ACP</td>
<td>
<a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level">COPP_ACP_Protection_Level</a>
</td>
</tr>
<tr>
<td>CGMS-A</td>
<td>
<a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level">COPP_CGMSA_Protection_Level</a>
</td>
</tr>
<tr>
<td>HDCP</td>
<td>
<a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level">COPP_HDCP_Protection_Level</a>
</td>
</tr>
</table>

### -field ExtendedInfoChangeMask

Reserved. Must be zero.

### -field ExtendedInfoData

Reserved. Must be zero.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>