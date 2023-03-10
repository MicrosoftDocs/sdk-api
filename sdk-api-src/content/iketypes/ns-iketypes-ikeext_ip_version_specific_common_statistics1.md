---
UID: NS:iketypes.IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1_
title: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1 (iketypes.h)
description: Various statistics common to the keying module (IKE, Authip, and IKEv2).
helpviewer_keywords: ["IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1","IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1 structure [Filtering]","fwp.ikeext_ip_version_specific_common_statistics1","iketypes/IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1"]
old-location: fwp\ikeext_ip_version_specific_common_statistics1.htm
tech.root: fwp
ms.assetid: 58e109fd-8a32-47bd-bc6a-bbe1bb54bc7e
ms.date: 12/05/2018
ms.keywords: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1, IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1 structure [Filtering], fwp.ikeext_ip_version_specific_common_statistics1, iketypes/IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
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
targetos: Windows
req.typenames: IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1_
 - iketypes/IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1_
 - IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
 - iketypes/IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1
---

# IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1 structure


## -description

The <b>IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS1</b> structure contains various statistics common to the keying module (IKE,  Authip, and IKEv2).
[IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) is available.</div><div> </div>

## -struct-fields

### -field totalSocketReceiveFailures

Total number of UDP 500/4500 socket receive failures.

### -field totalSocketSendFailures

Total number of UDP 500/4500 socket send failures.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>