---
UID: NS:opmapi._OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
title: "_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS"
author: windows-sdk-content
description: Contains parameters for the IOPMVideoOutput::COPPCompatibleGetInformation method.
old-location: mf\opm_copp_compatible_get_info_parameters.htm
tech.root: MedFound
ms.assetid: 20094e3d-3140-451a-a572-c268ad4c50c1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS, OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS structure [Media Foundation], _OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS, mf.opm_copp_compatible_get_info_parameters, opmapi/OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
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
 - OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
product: Windows
targetos: Windows
req.typenames: OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS
req.redist: 
---

# _OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS structure


## -description


Contains parameters for the <a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">IOPMVideoOutput::COPPCompatibleGetInformation</a> method.


## -struct-fields




### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure that contains a cryptographically secure 128-bit random number.


### -field guidInformation

A GUID that defines the status request. For more information, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


### -field ulSequenceNumber

The sequence number of the status request. The application must keep a running count of status requests. For each request, increment the sequence number by one.

On the first call to <a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">COPPCompatibleGetInformation</a>, set <b>ulSequenceNumber</b> equal to the starting sequence number, which is specified when the application calls <a href="https://msdn.microsoft.com/eeedeb4b-753f-4efb-b8ef-732cce116b42">IOPMVideoOutput::FinishInitialization</a>. On each subsequent call, increment <b>ulSequenceNumber</b> by 1.


### -field cbParametersSize

The number of bytes of valid data in the <b>abParameters</b> member.


### -field abParameters

The data for the status request. The meaning of the data depends on the request. For more information, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/988e6d54-f241-4cfc-8793-fc42de92ac52">AMCOPPStatusInput</a> structure used in COPP.




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

