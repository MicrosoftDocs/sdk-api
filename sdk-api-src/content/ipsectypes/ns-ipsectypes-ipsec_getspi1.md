---
UID: NS:ipsectypes.IPSEC_GETSPI1_
title: IPSEC_GETSPI1 (ipsectypes.h)
description: The IPSEC_GETSPI1 structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.Note  IPSEC_GETSPI1 is the specific implementation of IPSEC_GETSPI used in Windows 7 and later.
helpviewer_keywords: ["IPSEC_GETSPI1","IPSEC_GETSPI1 structure [Filtering]","fwp.ipsec_getspi1","ipsectypes/IPSEC_GETSPI1"]
old-location: fwp\ipsec_getspi1.htm
tech.root: fwp
ms.assetid: 671a8dd2-b4f6-4bdd-a6f1-1bf4260c6cbe
ms.date: 12/05/2018
ms.keywords: IPSEC_GETSPI1, IPSEC_GETSPI1 structure [Filtering], fwp.ipsec_getspi1, ipsectypes/IPSEC_GETSPI1
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: IPSEC_GETSPI1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_GETSPI1_
 - ipsectypes/IPSEC_GETSPI1_
 - IPSEC_GETSPI1
 - ipsectypes/IPSEC_GETSPI1
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
 - IPSEC_GETSPI1
---

# IPSEC_GETSPI1 structure


## -description

The <b>IPSEC_GETSPI1</b> structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.
[IPSEC_GETSPI0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_getspi0) is available.</div><div> </div>

## -struct-fields

### -field inboundIpsecTraffic

An [IPSEC_TRAFFIC1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1) structure that describes traffic characteristics of the inbound IPsec SA.

### -field ipVersion

An [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version) value that indicates the IP version of the inbound IPsec traffic.

### -field inboundUdpEncapsulation

Optional [IPSEC_V4_UDP_ENCAPSULATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0) structure that specifies the IPsec NAT Traversal (NATT) UDP encapsulation ports. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field rngCryptoModuleID

Not used. An <b>IPSEC_CRYPTO_MODULE_ID</b> is a <b>GUID</b> value.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>