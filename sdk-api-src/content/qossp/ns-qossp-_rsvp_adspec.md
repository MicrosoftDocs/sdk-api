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

# _RSVP_ADSPEC structure


## -description


<p class="CCE_Message">[The RSVP_ADSPEC QOS object is not supported except on Windows 2000. RSVP signaling is not supported except on Windows 2000.]

The QOS object 
<b>RSVP_ADSPEC</b> provides a means by which information describing network devices along the data path between sender and receiver, pertaining to RSVP functionality and available services, is provided or retrieved.


## -struct-fields




### -field ObjectHdr

The QOS object 
<b>QOS_OBJECT_HDR</b>.


### -field GeneralParams

An <a href="https://msdn.microsoft.com/eab6b317-9d06-45e2-bc77-0882f40e7d79">AD_GENERAL_PARAMS</a> structure that provides general characterization parameters for the flow. Information includes RSVP-enabled hop count, bandwidth and latency estimates, and the path's MTU.


### -field NumberOfServices

Provides a count of the number of services available.


### -field Services

A <a href="https://msdn.microsoft.com/604d7be8-955b-40a3-9cb4-6cbfbeeaa105">CONTROL_SERVICE</a> array, its element count based on <b>NumberOfServices</b>, which provides information about the services available along the data path between the sender and receiver of a given flow.


## -see-also




<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>
 

 

