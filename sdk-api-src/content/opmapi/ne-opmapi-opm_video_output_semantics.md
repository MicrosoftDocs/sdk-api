---
UID: NE:opmapi._OPM_VIDEO_OUTPUT_SEMANTICS
title: OPM_VIDEO_OUTPUT_SEMANTICS (opmapi.h)
description: Specifies whether the IOPMVideoOutput interface will use Output Protection Manager (OPM) semantics or Certified Output Protection Protocol (COPP) semantics.
helpviewer_keywords: ["OPM_VIDEO_OUTPUT_SEMANTICS","OPM_VIDEO_OUTPUT_SEMANTICS enumeration [Media Foundation]","OPM_VOS_COPP_SEMANTICS","OPM_VOS_OPM_SEMANTICS","mf.opm_video_output_semantics","opmapi/OPM_VIDEO_OUTPUT_SEMANTICS","opmapi/OPM_VOS_COPP_SEMANTICS","opmapi/OPM_VOS_OPM_SEMANTICS"]
old-location: mf\opm_video_output_semantics.htm
tech.root: mf
ms.assetid: d52fbc40-072b-4b7a-87c2-b928563100bb
ms.date: 12/05/2018
ms.keywords: OPM_VIDEO_OUTPUT_SEMANTICS, OPM_VIDEO_OUTPUT_SEMANTICS enumeration [Media Foundation], OPM_VOS_COPP_SEMANTICS, OPM_VOS_OPM_SEMANTICS, mf.opm_video_output_semantics, opmapi/OPM_VIDEO_OUTPUT_SEMANTICS, opmapi/OPM_VOS_COPP_SEMANTICS, opmapi/OPM_VOS_OPM_SEMANTICS
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
req.typenames: OPM_VIDEO_OUTPUT_SEMANTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_VIDEO_OUTPUT_SEMANTICS
 - opmapi/_OPM_VIDEO_OUTPUT_SEMANTICS
 - OPM_VIDEO_OUTPUT_SEMANTICS
 - opmapi/OPM_VIDEO_OUTPUT_SEMANTICS
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
 - OPM_VIDEO_OUTPUT_SEMANTICS
---

# OPM_VIDEO_OUTPUT_SEMANTICS enumeration


## -description

Specifies whether the <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput">IOPMVideoOutput</a> interface will use Output Protection Manager (OPM) semantics or Certified Output Protection Protocol (COPP) semantics.

## -enum-fields

### -field OPM_VOS_COPP_SEMANTICS:0

The interface will use COPP semantics.

### -field OPM_VOS_OPM_SEMANTICS:1

The interface will use OPM semantics.

### -field OPM_VOS_OPM_INDIRECT_DISPLAY:2

## -see-also

<a href="/windows/desktop/medfound/opm-enumerations">OPM Enumerations</a>



<a href="/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor">OPMGetVideoOutputsFromHMONITOR</a>



<a href="/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object">OPMGetVideoOutputsFromIDirect3DDevice9Object</a>
