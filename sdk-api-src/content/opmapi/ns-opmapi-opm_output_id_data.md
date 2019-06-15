---
UID: NS:opmapi._OPM_OUTPUT_ID_DATA
title: OPM_OUTPUT_ID_DATA (opmapi.h)
author: windows-sdk-content
description: Contains the result from an OPM_GET_OUTPUT_ID status request.
old-location: mf\opm_output_id_data.htm
tech.root: medfound
ms.assetid: 3fb56b5d-470c-4ca2-bf8b-5c3761c7cf06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OPM_OUTPUT_ID_DATA, OPM_OUTPUT_ID_DATA structure [Media Foundation], mf.opm_output_id_data, opmapi/OPM_OUTPUT_ID_DATA
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_OUTPUT_ID_DATA
product: Windows
targetos: Windows
req.typenames: OPM_OUTPUT_ID_DATA
req.redist: 
ms.custom: 19H1
---

# OPM_OUTPUT_ID_DATA structure


## -description


Contains the result from an <a href="https://docs.microsoft.com/windows/desktop/medfound/opm-get-output-id">OPM_GET_OUTPUT_ID</a> status request.


## -struct-fields




### -field rnRandomNumber

An <a href="https://docs.microsoft.com/windows/desktop/api/ksopmapi/ns-ksopmapi-_opm_random_number">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://docs.microsoft.com/windows/desktop/api/ksopmapi/ns-ksopmapi-_opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> or <a href="https://docs.microsoft.com/windows/desktop/api/opmapi/ns-opmapi-_opm_copp_compatible_get_info_parameters">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.


### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="https://docs.microsoft.com/windows/desktop/medfound/opm-status-flags">OPM Status Flags</a>.




### -field OutputId

The unique identifier of the monitor associated with this video output.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
 

 

