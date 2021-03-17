---
UID: NS:ipsectypes.IPSEC_SA_IDLE_TIMEOUT0_
title: IPSEC_SA_IDLE_TIMEOUT0 (ipsectypes.h)
description: The security association (SA) idle timeout in IPsec policy.
helpviewer_keywords: ["IPSEC_SA_IDLE_TIMEOUT0","IPSEC_SA_IDLE_TIMEOUT0 structure [Filtering]","fwp.ipsec_sa_idle_timeout0","ipsectypes/IPSEC_SA_IDLE_TIMEOUT0"]
old-location: fwp\ipsec_sa_idle_timeout0.htm
tech.root: fwp
ms.assetid: 99113c80-1e2a-4878-9b18-502cfb1e43cc
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_IDLE_TIMEOUT0, IPSEC_SA_IDLE_TIMEOUT0 structure [Filtering], fwp.ipsec_sa_idle_timeout0, ipsectypes/IPSEC_SA_IDLE_TIMEOUT0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_SA_IDLE_TIMEOUT0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_IDLE_TIMEOUT0_
 - ipsectypes/IPSEC_SA_IDLE_TIMEOUT0_
 - IPSEC_SA_IDLE_TIMEOUT0
 - ipsectypes/IPSEC_SA_IDLE_TIMEOUT0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_SA_IDLE_TIMEOUT0
---

# IPSEC_SA_IDLE_TIMEOUT0 structure


## -description

The <b>IPSEC_SA_IDLE_TIMEOUT0</b> structure specifies the security association (SA) idle timeout in IPsec policy.

## -struct-fields

### -field idleTimeoutSeconds

Specifies the amount of time in seconds after which IPsec SAs should become  idle.

### -field idleTimeoutSecondsFailOver

Specifies the amount of time in seconds after which IPsec SAs should become idle if the peer machine supports fail over.

## -remarks

<b>IPSEC_SA_IDLE_TIMEOUT0</b> is a specific implementation of IPSEC_SA_IDLE_TIMEOUT. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.