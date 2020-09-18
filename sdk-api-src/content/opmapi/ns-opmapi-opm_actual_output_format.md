---
UID: NS:opmapi._OPM_ACTUAL_OUTPUT_FORMAT
title: OPM_ACTUAL_OUTPUT_FORMAT (opmapi.h)
description: Contains the result of an OPM_GET_ACTUAL_OUTPUT_FORMAT query in Output Protection Manager (OPM).
helpviewer_keywords: ["OPM_ACTUAL_OUTPUT_FORMAT","OPM_ACTUAL_OUTPUT_FORMAT structure [Media Foundation]","mf.opm_actual_output_format","opmapi/OPM_ACTUAL_OUTPUT_FORMAT"]
old-location: mf\opm_actual_output_format.htm
tech.root: mf
ms.assetid: 0b20cdcd-3d03-4da3-b81c-b5025dcb04c3
ms.date: 12/05/2018
ms.keywords: OPM_ACTUAL_OUTPUT_FORMAT, OPM_ACTUAL_OUTPUT_FORMAT structure [Media Foundation], mf.opm_actual_output_format, opmapi/OPM_ACTUAL_OUTPUT_FORMAT
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
req.typenames: OPM_ACTUAL_OUTPUT_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_ACTUAL_OUTPUT_FORMAT
 - opmapi/_OPM_ACTUAL_OUTPUT_FORMAT
 - OPM_ACTUAL_OUTPUT_FORMAT
 - opmapi/OPM_ACTUAL_OUTPUT_FORMAT
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
 - OPM_ACTUAL_OUTPUT_FORMAT
---

# OPM_ACTUAL_OUTPUT_FORMAT structure


## -description

Contains the result of an <a href="/windows/desktop/medfound/opm-get-actual-output-format">OPM_GET_ACTUAL_OUTPUT_FORMAT</a> query in <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM).

## -struct-fields

### -field rnRandomNumber

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> or <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.

### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="/windows/desktop/medfound/opm-status-flags">OPM Status Flags</a>.

### -field ulDisplayWidth

The width of the display mode, in pixels.

### -field ulDisplayHeight

The height of the display mode, in pixels.

### -field dsfSampleInterleaveFormat

A <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat">DXVA2_SampleFormat</a> value that describes the interlace mode.

### -field d3dFormat

A <b>D3DFORMAT</b> value that describes the video format.

### -field ulFrequencyNumerator

The numerator of the refresh rate of the current display mode.

### -field ulFrequencyDenominator

The denominator of the refresh rate of the current display mode.

## -remarks

The refresh rate is expressed as a fraction. For example, if the refresh rate is 72 Hz, <b>FreqNumerator</b> = 72 and <b>FreqDenominator</b> = 1. For NTSC television, the values are <b>FreqNumerator</b> = 60000 and <b>FreqDenominator</b> = 1001 (59.94 fields per second). 

The layout of this structure is identical to the <a href="/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata">DXVA_COPPStatusDisplayData</a> structure used in Certified Output Protection Protocol (COPP).

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>