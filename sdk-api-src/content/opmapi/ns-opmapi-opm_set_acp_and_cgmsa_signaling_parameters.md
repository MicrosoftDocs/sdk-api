---
UID: NS:opmapi._OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
title: OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS (opmapi.h)
description: Contains information for the OPM_SET_ACP_AND_CGMSA_SIGNALING command in Output Protection Manager (OPM).
helpviewer_keywords: ["OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS","OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS structure [Media Foundation]","mf.opm_set_acp_and_cgmsa_signaling_parameters","opmapi/OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS"]
old-location: mf\opm_set_acp_and_cgmsa_signaling_parameters.htm
tech.root: mf
ms.assetid: bb7caedd-cd9e-4b36-b1a1-a457de44afb1
ms.date: 12/05/2018
ms.keywords: OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS, OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS structure [Media Foundation], mf.opm_set_acp_and_cgmsa_signaling_parameters, opmapi/OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
req.header: opmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
 - opmapi/_OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
 - OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
 - opmapi/OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS
---

# OPM_SET_ACP_AND_CGMSA_SIGNALING_PARAMETERS structure


## -description

Contains information for the <a href="/windows/desktop/medfound/opm-set-acp-and-cgmsa-signaling">OPM_SET_ACP_AND_CGMSA_SIGNALING</a> command in <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM).

This command causes the driver to insert Wide Screen Signaling (WSS) codes or other data packets in the television signal, as required by some Analog Copy Protection (ACP) and Copy Generation Management System — Analog (CGMS-A) specifications. For example:
<ul>
<li>ETSI EN 300 294 (625i PAL): Data packets are inserted into line 23 of the signal.</li>
<li>CEA-608-B (NTSC): Data packets are inserted into line 21 of the vertical blanking interval (VBI).</li>
</ul>

## -struct-fields

### -field ulNewTVProtectionStandard

Specifies the protection standard and format that is currently active. The value is a bitwise <b>OR</b> of <a href="/windows/desktop/medfound/tv-protection-standard-flags">TV Protection Standard Flags</a>.

### -field ulAspectRatioChangeMask1

A bitmask indicating which bits from <b>ulAspectRatioData1</b> to set in the signal.

### -field ulAspectRatioData1

Specifies the aspect ratio value to be set for the current protection standard. For EN 300 294, use the <a href="/windows/desktop/api/opmapi/ne-opmapi-opm_image_aspect_ratio_en300294">OPM_IMAGE_ASPECT_RATIO_EN300294</a> enumeration.

### -field ulAspectRatioChangeMask2

A bitmask indicating which bits from <b>ulAspectRatioData2</b> to set in the signal.

### -field ulAspectRatioData2

An additional data element related to aspect ratio. The presence and meaning of this data depends on the protection standard. This field can be used to convey End and Q0 bits for EIA-608-B, or the active format description for CEA-805-A.

### -field ulAspectRatioChangeMask3

A bitmask indicating which bits from <b>ulAspectRatioData3</b> to set in the signal.

### -field ulAspectRatioData3

An additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard.

### -field ulReserved

Reserved for future use. Set the entire array to zero.

### -field ulReserved2

Reserved for future use. Set the entire array to zero.

### -field ulReserved3

Reserved for future use. Set to zero.

## -remarks

The layout of this structure is identical to the <a href="/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata">DXVA_COPPSetSignalingCmdData</a> structure used in Certified Output Protection Manager (COPP).

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>