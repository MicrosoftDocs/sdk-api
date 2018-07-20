---
UID: NS:opmapi._OPM_STANDARD_INFORMATION
title: "_OPM_STANDARD_INFORMATION"
author: windows-sdk-content
description: Contains the result from an Output Protection Manager (OPM) status request.
old-location: mf\opm_standard_information.htm
old-project: medfound
ms.assetid: 4c1b6803-0015-4def-acb0-295193ba0e17
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OPM_STANDARD_INFORMATION, OPM_STANDARD_INFORMATION structure [Media Foundation], _OPM_STANDARD_INFORMATION, ksopmapi/OPM_STANDARD_INFORMATION, mf.opm_standard_information
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: OPM_STANDARD_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_STANDARD_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _OPM_STANDARD_INFORMATION structure


## -description


Contains the result from an <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM) status request.


## -struct-fields




### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://msdn.microsoft.com/8959c7d1-9a78-497f-8841-d3e61e9db6a3">OPM_GET_INFO_PARAMETERS</a> or <a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.


### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/d6d85fd4-e735-4610-93e0-bb2b1782f11b">OPM Status Flags</a>.


### -field ulInformation

Response data. The meaning of this value depends on the status request. For more information, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


### -field ulReserved

Reserved for future use. Set to zero.


### -field ulReserved2

Reserved for future use. Set to zero.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563154">DXVA_COPPStatusData</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

