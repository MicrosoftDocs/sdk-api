---
UID: NS:iketypes.IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0_
title: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0_
author: windows-sdk-content
description: Various statistics common to IKE and Authip.
old-location: fwp\ikeext_ip_version_specific_common_statistics0.htm
tech.root: fwp
ms.assetid: 0cacb7de-9f20-47ac-b040-8d65ede3bef3
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0, IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0 structure [Filtering], IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0_, fwp.ikeext_ip_version_specific_common_statistics0, iketypes/IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0
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
 - IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0
product: Windows
targetos: Windows
req.typenames: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0
req.redist: 
---

# IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0_ structure


## -description


The <b>IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0</b> structure contains various statistics common to IKE and Authip.
<div class="alert"><b>Note</b>  <b>IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0</b> is the specific implementation of IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/58e109fd-8a32-47bd-bc6a-bbe1bb54bc7e">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field totalSocketReceiveFailures

Total number of UDP 500/4500 socket receive failures.


### -field totalSocketSendFailures

Total number of UDP 500/4500 socket send failures.

