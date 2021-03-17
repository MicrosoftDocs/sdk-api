---
UID: NS:opmapi._OPM_ACP_AND_CGMSA_SIGNALING
title: OPM_ACP_AND_CGMSA_SIGNALING (opmapi.h)
description: Contains the result from an OPM_GET_ACP_AND_CGMSA_SIGNALING query.
helpviewer_keywords: ["OPM_ACP_AND_CGMSA_SIGNALING","OPM_ACP_AND_CGMSA_SIGNALING structure [Media Foundation]","mf.opm_acp_and_cgmsa_signaling","opmapi/OPM_ACP_AND_CGMSA_SIGNALING"]
old-location: mf\opm_acp_and_cgmsa_signaling.htm
tech.root: mf
ms.assetid: 7388bdd9-a8bc-45f4-8539-a175190fb3c3
ms.date: 12/05/2018
ms.keywords: OPM_ACP_AND_CGMSA_SIGNALING, OPM_ACP_AND_CGMSA_SIGNALING structure [Media Foundation], mf.opm_acp_and_cgmsa_signaling, opmapi/OPM_ACP_AND_CGMSA_SIGNALING
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
req.typenames: OPM_ACP_AND_CGMSA_SIGNALING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_ACP_AND_CGMSA_SIGNALING
 - opmapi/_OPM_ACP_AND_CGMSA_SIGNALING
 - OPM_ACP_AND_CGMSA_SIGNALING
 - opmapi/OPM_ACP_AND_CGMSA_SIGNALING
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
 - OPM_ACP_AND_CGMSA_SIGNALING
---

# OPM_ACP_AND_CGMSA_SIGNALING structure


## -description

Contains the result from an <a href="/windows/desktop/medfound/opm-get-acp-and-cgmsa-signaling">OPM_GET_ACP_AND_CGMSA_SIGNALING</a> query.

## -struct-fields

### -field rnRandomNumber

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> or <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.

### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="/windows/desktop/medfound/opm-status-flags">OPM Status Flags</a>.

### -field ulAvailableTVProtectionStandards

A bitwise <b>OR</b> of zero or more <a href="/windows/desktop/medfound/tv-protection-standard-flags">TV Protection Standard Flags</a>. The driver will return flags for all of the protection standards and resolutions that it supports, regardless of which are now active.

### -field ulActiveTVProtectionStandard

One value from the <a href="/windows/desktop/medfound/tv-protection-standard-flags">TV Protection Standard Flags</a>, indicating the protection standard that is currently active.

### -field ulReserved

Reserved for future use. Set to zero.

### -field ulAspectRatioValidMask1

A bitmask indicating which bits of <b>ulAspectRatioData1</b> are valid.

### -field ulAspectRatioData1

The current aspect ratio. For EN 300 294, the value is a member of the <a href="/windows/desktop/api/opmapi/ne-opmapi-opm_image_aspect_ratio_en300294">OPM_IMAGE_ASPECT_RATIO_EN300294</a> enumeration.

### -field ulAspectRatioValidMask2

A bitmask indicating which bits of <b>ulAspectRatioData2</b> are valid.

### -field ulAspectRatioData2

An additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard. This field can be used to convey End and Q0 bits for EIA-608-B, or the active format description for CEA-805-A.

### -field ulAspectRatioValidMask3

A bitmask indicating which bits of <b>ulAspectRatioData3</b> are valid.

### -field ulAspectRatioData3

An additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard.

### -field ulReserved2

Reserved for future use. Fill this array with zeros.

### -field ulReserved3

Reserved for future use.Fill this array with zeros.

## -remarks

The layout of this structure is identical to the <a href="/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata">DXVA_COPPStatusSignalingCmdData</a> structure used in Certified Output Protection Protocol (COPP).

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>