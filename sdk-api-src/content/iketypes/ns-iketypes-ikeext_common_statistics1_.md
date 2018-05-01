---
UID: NS:iketypes.IKEEXT_COMMON_STATISTICS1_
title: IKEEXT_COMMON_STATISTICS1_
author: windows-driver-content
description: Various statistics common to IKE, Authip, and IKEv2.
old-location: fwp\ikeext_common_statistics1.htm
old-project: FWP
ms.assetid: d2c473d7-921f-4175-8406-8ab24d7f74f4
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: IKEEXT_COMMON_STATISTICS1, IKEEXT_COMMON_STATISTICS1 structure [Filtering], IKEEXT_COMMON_STATISTICS1_, fwp.ikeext_common_statistics1, iketypes/IKEEXT_COMMON_STATISTICS0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_COMMON_STATISTICS1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_COMMON_STATISTICS1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_COMMON_STATISTICS1_ structure


## -description


The <b>IKEEXT_COMMON_STATISTICS1</b> structure contains various statistics common to IKE, Authip, and IKEv2.
<div class="alert"><b>Note</b>  <b>IKEEXT_COMMON_STATISTICS1</b> is the specific implementation of IKEEXT_COMMON_STATISTICS used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/a53ef735-3223-4ff5-9b2a-d40ab0f53570">IKEEXT_COMMON_STATISTICS0</a> is available.</div><div> </div>

## -struct-fields




### -field v4Statistics

IPv4 common statistics.

See <a href="https://msdn.microsoft.com/58e109fd-8a32-47bd-bc6a-bbe1bb54bc7e">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1</a> for more information.


### -field v6Statistics

IPv6 common statistics.

See <a href="https://msdn.microsoft.com/58e109fd-8a32-47bd-bc6a-bbe1bb54bc7e">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1</a> for more information.


### -field totalPacketsReceived

Total number of packets received.


### -field totalInvalidPacketsReceived

Total number of invalid packets received.


### -field currentQueuedWorkitems

Current number of work items that are queued and waiting to be processed.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

