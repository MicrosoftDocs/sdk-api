---
UID: NS:opmapi._OPM_GET_INFO_PARAMETERS
title: "_OPM_GET_INFO_PARAMETERS"
author: windows-sdk-content
description: Contains parameters for the IOPMVideoOutput::GetInformation method.
old-location: mf\opm_get_info_parameters.htm
tech.root: medfound
ms.assetid: 8959c7d1-9a78-497f-8841-d3e61e9db6a3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: OPM_GET_INFO_PARAMETERS, OPM_GET_INFO_PARAMETERS structure [Media Foundation], _OPM_GET_INFO_PARAMETERS, ksopmapi/OPM_GET_INFO_PARAMETERS, mf.opm_get_info_parameters
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_GET_INFO_PARAMETERS
product: Windows
targetos: Windows
req.typenames: OPM_GET_INFO_PARAMETERS
req.redist: 
---

# _OPM_GET_INFO_PARAMETERS structure


## -description


Contains parameters for the <a href="https://msdn.microsoft.com/47d724eb-07e9-4659-886a-4b492fbb2415">IOPMVideoOutput::GetInformation</a> method.


## -struct-fields




### -field omac

An <a href="https://msdn.microsoft.com/6ff37a2a-9e63-4097-8ee6-bcc4bd580ab8">OPM_OMAC</a> structure that contains a message authentication code (MAC) for the data in the rest of the structure.


### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure that contains a cryptographically secure 128-bit random number.


### -field guidInformation

A GUID that defines the status request. For more information, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


### -field ulSequenceNumber

The status sequence number. The application must keep a running count of status requests. For each request, increment the sequence number by 1.

On the first call to <a href="https://msdn.microsoft.com/47d724eb-07e9-4659-886a-4b492fbb2415">GetInformation</a>, set <b>ulSequenceNumber</b> equal to the starting status sequence number, which is specified when the application calls <a href="https://msdn.microsoft.com/eeedeb4b-753f-4efb-b8ef-732cce116b42">IOPMVideoOutput::FinishInitialization</a>. On each subsequent call, increment <b>ulSequenceNumber</b> by 1.

Exception: If the status request fails, do not increment the sequence number. Instead, re-use the same number for the next status request.


### -field cbParametersSize

The number of bytes of valid data in the <b>abParameters</b> member.


### -field abParameters

The data for the status request. The meaning of the data depends on the request. For more information, see <a href="https://msdn.microsoft.com/428d08c6-e9f0-49fb-9ef9-d0f95416669d">OPM Status Requests</a>.


## -remarks



Initialize this structure as follows:

<ol>
<li>Generate a cryptographically secure 128-bit random number and copy it to the <b>rnRandomNumber</b> member. Do not re-use this number after calling <a href="https://msdn.microsoft.com/47d724eb-07e9-4659-886a-4b492fbb2415">GetInformation</a>.</li>
<li>Fill in the remaining structure members, except for the <b>omac</b> member.</li>
<li>Use the OMAC 1 algorithm to calculate a message authentication code (MAC) for the block of data that appears after the <b>omac</b> member (excluding the <b>omac</b> member).</li>
<li>Copy the MAC to the <b>omac</b> member.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

