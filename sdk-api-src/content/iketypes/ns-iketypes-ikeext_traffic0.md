---
UID: NS:iketypes.IKEEXT_TRAFFIC0_
title: IKEEXT_TRAFFIC0 (iketypes.h)
description: Specifies the IKE/Authip traffic.
helpviewer_keywords: ["IKEEXT_TRAFFIC0","IKEEXT_TRAFFIC0 structure [Filtering]","fwp.ikeext_traffic0","iketypes/IKEEXT_TRAFFIC0"]
old-location: fwp\ikeext_traffic0.htm
tech.root: fwp
ms.assetid: 99cb3774-7afd-44fd-9c3e-e2d913aaeecb
ms.date: 12/05/2018
ms.keywords: IKEEXT_TRAFFIC0, IKEEXT_TRAFFIC0 structure [Filtering], fwp.ikeext_traffic0, iketypes/IKEEXT_TRAFFIC0
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
targetos: Windows
req.typenames: IKEEXT_TRAFFIC0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_TRAFFIC0_
 - iketypes/IKEEXT_TRAFFIC0_
 - IKEEXT_TRAFFIC0
 - iketypes/IKEEXT_TRAFFIC0
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
 - IKEEXT_TRAFFIC0
---

# IKEEXT_TRAFFIC0 structure


## -description

The <b>IKEEXT_TRAFFIC0</b> structure specifies the IKE/Authip traffic.

## -struct-fields

### -field ipVersion

IP version specified by [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version).

### -field localV4Address

The local address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field localV6Address

The local address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.

### -field remoteV4Address

The remote address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field remoteV6Address

The remote address of the traffic. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.

### -field authIpFilterId

   Filter ID from quick mode (QM) policy of matching extended mode (EM) filter.

## -remarks

<b>IKEEXT_TRAFFIC0</b> is a specific implementation of IKEEXT_TRAFFIC. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>