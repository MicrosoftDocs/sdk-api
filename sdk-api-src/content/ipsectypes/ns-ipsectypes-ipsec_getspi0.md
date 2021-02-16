---
UID: NS:ipsectypes.IPSEC_GETSPI0_
title: IPSEC_GETSPI0 (ipsectypes.h)
description: The IPSEC_GETSPI0 structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.Note  IPSEC_GETSPI0 is the specific implementation of IPSEC_GETSPI used in Windows Vista.
helpviewer_keywords: ["IPSEC_GETSPI0","IPSEC_GETSPI0 structure [Filtering]","fwp.ipsec_getspi0","ipsectypes/IPSEC_GETSPI0"]
old-location: fwp\ipsec_getspi0.htm
tech.root: fwp
ms.assetid: a43c447c-83b4-4ca4-a7c5-7e10e6607692
ms.date: 12/05/2018
ms.keywords: IPSEC_GETSPI0, IPSEC_GETSPI0 structure [Filtering], fwp.ipsec_getspi0, ipsectypes/IPSEC_GETSPI0
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
req.typenames: IPSEC_GETSPI0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_GETSPI0_
 - ipsectypes/IPSEC_GETSPI0_
 - IPSEC_GETSPI0
 - ipsectypes/IPSEC_GETSPI0
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
 - IPSEC_GETSPI0
---

# IPSEC_GETSPI0 structure


## -description

The <b>IPSEC_GETSPI0</b> structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.
[IPSEC_GETSPI1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_getspi1) is available.</div><div> </div>

## -struct-fields

### -field inboundIpsecTraffic

An [IPSEC_TRAFFIC0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic0) structure that describes traffic characteristics of the inbound IPsec SA.

### -field ipVersion

A [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version) value that indicates the IP version of the inbound IPsec traffic.

### -field inboundUdpEncapsulation

Optional [IPSEC_V4_UDP_ENCAPSULATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0) structure that specifies the IPsec NAT Traversal (NATT) UDP encapsulation ports. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field rngCryptoModuleID

Not used. A <b>IPSEC_CRYPTO_MODULE_ID</b> is a <b>GUID</b> value.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>