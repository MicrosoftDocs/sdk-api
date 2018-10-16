---
UID: NS:iketypes.IKEEXT_COMMON_STATISTICS0_
title: IKEEXT_COMMON_STATISTICS0_
author: windows-sdk-content
description: Various statistics common to IKE and Authip.
old-location: fwp\ikeext_common_statistics0.htm
tech.root: fwp
ms.assetid: a53ef735-3223-4ff5-9b2a-d40ab0f53570
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IKEEXT_COMMON_STATISTICS0, IKEEXT_COMMON_STATISTICS0 structure [Filtering], IKEEXT_COMMON_STATISTICS0_, fwp.ikeext_common_statistics0, iketypes/IKEEXT_COMMON_STATISTICS0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
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
 - Iketypes.h
api_name:
 - IKEEXT_COMMON_STATISTICS0
product: Windows
targetos: Windows
req.typenames: IKEEXT_COMMON_STATISTICS0
req.redist: 
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

