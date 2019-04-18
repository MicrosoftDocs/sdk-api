---
UID: NS:iketypes.IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1_
title: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1 (iketypes.h)
author: windows-sdk-content
description: Various statistics common to the keying module (IKE, Authip, and IKEv2).
old-location: fwp\ikeext_ip_version_specific_common_statistics1.htm
tech.root: fwp
ms.assetid: 58e109fd-8a32-47bd-bc6a-bbe1bb54bc7e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1, IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1 structure [Filtering], fwp.ikeext_ip_version_specific_common_statistics1, iketypes/IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
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
 - IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
product: Windows
targetos: Windows
req.typenames: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
req.redist: 
ms.custom: 19H1
---

# IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1 structure


## -description


The <b>IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1</b> structure contains various statistics common to the keying module (IKE,  Authip, and IKEv2).
<div class="alert"><b>Note</b>  <b>IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1</b> is the specific implementation of IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/en-us/library/Aa365114(v=VS.85).aspx">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0</a> is available.</div><div> </div>

## -struct-fields




### -field totalSocketReceiveFailures

Total number of UDP 500/4500 socket receive failures.


### -field totalSocketSendFailures

Total number of UDP 500/4500 socket send failures.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

