---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

