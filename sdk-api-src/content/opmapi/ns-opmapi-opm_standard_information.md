---
UID: NS:opmapi._OPM_STANDARD_INFORMATION
title: OPM_STANDARD_INFORMATION (opmapi.h)
description: OPM_STANDARD_INFORMATION (opmapi.h) contains the result from an Output Protection Manager (OPM) status request.
helpviewer_keywords: ["OPM_STANDARD_INFORMATION","OPM_STANDARD_INFORMATION structure [Media Foundation]","_OPM_STANDARD_INFORMATION","ksopmapi/OPM_STANDARD_INFORMATION","mf.opm_standard_information"]
old-location: mf\opm_standard_information.htm
tech.root: mf
ms.assetid: 4c1b6803-0015-4def-acb0-295193ba0e17
ms.date: 08/02/2022
ms.keywords: OPM_STANDARD_INFORMATION, OPM_STANDARD_INFORMATION structure [Media Foundation], _OPM_STANDARD_INFORMATION, ksopmapi/OPM_STANDARD_INFORMATION, mf.opm_standard_information
req.header: opmapi.h
req.include-header: Opmapi.h
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
req.typenames: OPM_STANDARD_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_STANDARD_INFORMATION
 - opmapi/_OPM_STANDARD_INFORMATION
 - OPM_STANDARD_INFORMATION
 - opmapi/OPM_STANDARD_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_STANDARD_INFORMATION
---

# OPM_STANDARD_INFORMATION structure


## -description

Contains the result from an <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM) status request.

## -struct-fields

### -field rnRandomNumber

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> or <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.

### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="/windows/desktop/medfound/opm-status-flags">OPM Status Flags</a>.

### -field ulInformation

Response data. The meaning of this value depends on the status request. For more information, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

### -field ulReserved

Reserved for future use. Set to zero.

### -field ulReserved2

Reserved for future use. Set to zero.

## -remarks

The layout of this structure is identical to the <a href="/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata">DXVA_COPPStatusData</a> structure used in Certified Output Protection Protocol (COPP).

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
