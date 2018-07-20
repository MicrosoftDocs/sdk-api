---
UID: NS:opmapi._OPM_OUTPUT_ID_DATA
title: "_OPM_OUTPUT_ID_DATA"
author: windows-sdk-content
description: Contains the result from an OPM_GET_OUTPUT_ID status request.
old-location: mf\opm_output_id_data.htm
old-project: medfound
ms.assetid: 3fb56b5d-470c-4ca2-bf8b-5c3761c7cf06
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OPM_OUTPUT_ID_DATA, OPM_OUTPUT_ID_DATA structure [Media Foundation], _OPM_OUTPUT_ID_DATA, mf.opm_output_id_data, opmapi/OPM_OUTPUT_ID_DATA
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: OPM_OUTPUT_ID_DATA
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _OPM_OUTPUT_ID_DATA structure


## -description


Contains the result from an <a href="https://msdn.microsoft.com/d34d68ff-c513-483e-8619-4a9baa2a40ba">OPM_GET_OUTPUT_ID</a> status request.


## -struct-fields




### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://msdn.microsoft.com/8959c7d1-9a78-497f-8841-d3e61e9db6a3">OPM_GET_INFO_PARAMETERS</a> or <a href="https://msdn.microsoft.com/20094e3d-3140-451a-a572-c268ad4c50c1">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.


### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/d6d85fd4-e735-4610-93e0-bb2b1782f11b">OPM Status Flags</a>.




### -field OutputId

The unique identifier of the monitor associated with this video output.


## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

