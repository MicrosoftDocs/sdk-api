---
UID: NS:ksopmapi._OPM_REQUESTED_INFORMATION
title: OPM_REQUESTED_INFORMATION (ksopmapi.h)
description: The OPM_REQUESTED_INFORMATION (ksopmapi.h) structure contains the result of an Output Protection Manager (OPM) status request.
helpviewer_keywords: ["OPM_REQUESTED_INFORMATION","OPM_REQUESTED_INFORMATION structure [Media Foundation]","_OPM_REQUESTED_INFORMATION","ksopmapi/OPM_REQUESTED_INFORMATION","mf.opm_requested_information"]
old-location: mf\opm_requested_information.htm
tech.root: mf
ms.assetid: 84ffa808-1bdb-47c8-a18c-6dfa6fcf90de
ms.date: 08/05/2022
ms.keywords: OPM_REQUESTED_INFORMATION, OPM_REQUESTED_INFORMATION structure [Media Foundation], _OPM_REQUESTED_INFORMATION, ksopmapi/OPM_REQUESTED_INFORMATION, mf.opm_requested_information
req.header: ksopmapi.h
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
req.typenames: OPM_REQUESTED_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_REQUESTED_INFORMATION
 - ksopmapi/_OPM_REQUESTED_INFORMATION
 - OPM_REQUESTED_INFORMATION
 - ksopmapi/OPM_REQUESTED_INFORMATION
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
 - OPM_REQUESTED_INFORMATION
---

# OPM_REQUESTED_INFORMATION structure


## -description

Contains the result of an <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM) status request.

## -struct-fields

### -field omac

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac">OPM_OMAC</a> structure that contains a Message Authentication Code (MAC) of the status data. The driver will use AES-based one-key CBC MAC (OMAC) to calculate this value.

### -field cbRequestedInformationSize

The size of the valid data in the <b>abRequestedInformation</b> member, in bytes.

### -field abRequestedInformation

A buffer that contains the result of the status request. The meaning of the data depends on the status request. For more information, see <a href="/windows/desktop/medfound/opm-status-requests">OPM Status Requests</a>.

## -remarks

The layout of this structure is identical to the <a href="/windows/desktop/api/strmif/ns-strmif-amcoppstatusoutput">AMCOPPStatusOutput</a> structure used in Certified Output Protection Protocol (COPP).

## -see-also

<a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">IOPMVideoOutput::COPPCompatibleGetInformation</a>



<a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation">IOPMVideoOutput::GetInformation</a>



<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
