---
UID: NS:opmapi._OPM_GET_INFO_PARAMETERS
title: OPM_GET_INFO_PARAMETERS (opmapi.h)
description: OPM_GET_INFO_PARAMETERS (opmapi.h) contains parameters for the IOPMVideoOutput::GetInformation method.
helpviewer_keywords: ["OPM_GET_INFO_PARAMETERS","OPM_GET_INFO_PARAMETERS structure [Media Foundation]","_OPM_GET_INFO_PARAMETERS","ksopmapi/OPM_GET_INFO_PARAMETERS","mf.opm_get_info_parameters"]
old-location: mf\opm_get_info_parameters.htm
tech.root: mf
ms.assetid: 8959c7d1-9a78-497f-8841-d3e61e9db6a3
ms.date: 08/02/2022
ms.keywords: OPM_GET_INFO_PARAMETERS, OPM_GET_INFO_PARAMETERS structure [Media Foundation], _OPM_GET_INFO_PARAMETERS, ksopmapi/OPM_GET_INFO_PARAMETERS, mf.opm_get_info_parameters
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
req.typenames: OPM_GET_INFO_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_GET_INFO_PARAMETERS
 - opmapi/_OPM_GET_INFO_PARAMETERS
 - OPM_GET_INFO_PARAMETERS
 - opmapi/OPM_GET_INFO_PARAMETERS
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
 - OPM_GET_INFO_PARAMETERS
---

# OPM_GET_INFO_PARAMETERS structure


## -description

Contains parameters for the <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation">IOPMVideoOutput::GetInformation</a> method.

## -struct-fields

### -field omac

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac">OPM_OMAC</a> structure that contains a message authentication code (MAC) for the data in the rest of the structure.

### -field rnRandomNumber

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure that contains a cryptographically secure 128-bit random number.

### -field guidInformation

A GUID that defines the status request. For more information, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

### -field ulSequenceNumber

The status sequence number. The application must keep a running count of status requests. For each request, increment the sequence number by 1.

On the first call to <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation">GetInformation</a>, set <b>ulSequenceNumber</b> equal to the starting status sequence number, which is specified when the application calls <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization">IOPMVideoOutput::FinishInitialization</a>. On each subsequent call, increment <b>ulSequenceNumber</b> by 1.

Exception: If the status request fails, do not increment the sequence number. Instead, re-use the same number for the next status request.

### -field cbParametersSize

The number of bytes of valid data in the <b>abParameters</b> member.

### -field abParameters

The data for the status request. The meaning of the data depends on the request. For more information, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

## -remarks

Initialize this structure as follows:

<ol>
<li>Generate a cryptographically secure 128-bit random number and copy it to the <b>rnRandomNumber</b> member. Do not re-use this number after calling <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation">GetInformation</a>.</li>
<li>Fill in the remaining structure members, except for the <b>omac</b> member.</li>
<li>Use the OMAC 1 algorithm to calculate a message authentication code (MAC) for the block of data that appears after the <b>omac</b> member (excluding the <b>omac</b> member).</li>
<li>Copy the MAC to the <b>omac</b> member.</li>
</ol>

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
