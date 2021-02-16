---
UID: NS:opmapi._OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
title: OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS (opmapi.h)
description: Contains parameters for the IOPMVideoOutput::COPPCompatibleGetInformation method.
helpviewer_keywords: ["OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS","OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS structure [Media Foundation]","mf.opm_copp_compatible_get_info_parameters","opmapi/OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS"]
old-location: mf\opm_copp_compatible_get_info_parameters.htm
tech.root: mf
ms.assetid: 20094e3d-3140-451a-a572-c268ad4c50c1
ms.date: 12/05/2018
ms.keywords: OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS, OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS structure [Media Foundation], mf.opm_copp_compatible_get_info_parameters, opmapi/OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
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
req.typenames: OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
 - opmapi/_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
 - OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
 - opmapi/OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
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
 - OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
---

# OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS structure


## -description

Contains parameters for the <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">IOPMVideoOutput::COPPCompatibleGetInformation</a> method.

## -struct-fields

### -field rnRandomNumber

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure that contains a cryptographically secure 128-bit random number.

### -field guidInformation

A GUID that defines the status request. For more information, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

### -field ulSequenceNumber

The sequence number of the status request. The application must keep a running count of status requests. For each request, increment the sequence number by one.

On the first call to <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">COPPCompatibleGetInformation</a>, set <b>ulSequenceNumber</b> equal to the starting sequence number, which is specified when the application calls <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization">IOPMVideoOutput::FinishInitialization</a>. On each subsequent call, increment <b>ulSequenceNumber</b> by 1.

### -field cbParametersSize

The number of bytes of valid data in the <b>abParameters</b> member.

### -field abParameters

The data for the status request. The meaning of the data depends on the request. For more information, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

## -remarks

The layout of this structure is identical to the <a href="/windows/desktop/api/strmif/ns-strmif-amcoppstatusinput">AMCOPPStatusInput</a> structure used in COPP.

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>