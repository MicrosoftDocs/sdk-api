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

# IKEEXT_COMMON_STATISTICS0_ structure


## -description


The <b>IKEEXT_COMMON_STATISTICS0</b> structure contains various statistics common to IKE and Authip.
<div class="alert"><b>Note</b>  <b>IKEEXT_COMMON_STATISTICS0</b> is the specific implementation of IKEEXT_COMMON_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/d2c473d7-921f-4175-8406-8ab24d7f74f4">IKEEXT_COMMON_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field v4Statistics

IPv4 common statistics.

See <a href="https://msdn.microsoft.com/0cacb7de-9f20-47ac-b040-8d65ede3bef3">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0</a> for more information.


### -field v6Statistics

IPv6 common statistics.

See <a href="https://msdn.microsoft.com/0cacb7de-9f20-47ac-b040-8d65ede3bef3">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0</a> for more information.


### -field totalPacketsReceived

Total number of packets received.


### -field totalInvalidPacketsReceived

Total number of invalid packets received.


### -field currentQueuedWorkitems

Current number of work items that are queued and waiting to be processed.

