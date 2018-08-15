---
UID: NS:ipsectypes.IPSEC_GETSPI0_
title: IPSEC_GETSPI0_
author: windows-sdk-content
description: The IPSEC_GETSPI0 structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.Note  IPSEC_GETSPI0 is the specific implementation of IPSEC_GETSPI used in Windows Vista.
old-location: fwp\ipsec_getspi0.htm
old-project: fwp
ms.assetid: a43c447c-83b4-4ca4-a7c5-7e10e6607692
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPSEC_GETSPI0, IPSEC_GETSPI0 structure [Filtering], IPSEC_GETSPI0_, fwp.ipsec_getspi0, ipsectypes/IPSEC_GETSPI0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: IPSEC_GETSPI0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_GETSPI0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_GETSPI0_ structure


## -description


The <b>IPSEC_GETSPI0</b> structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.
<div class="alert"><b>Note</b>  <b>IPSEC_GETSPI0</b> is the specific implementation of IPSEC_GETSPI used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/671a8dd2-b4f6-4bdd-a6f1-1bf4260c6cbe">IPSEC_GETSPI1</a> is available.</div><div> </div>

## -struct-fields




### -field inboundIpsecTraffic

An <a href="https://msdn.microsoft.com/5be2da29-73d6-4381-8bde-3a3945ea7b5a">IPSEC_TRAFFIC0</a> structure that describes traffic characteristics of the inbound IPsec SA.


### -field ipVersion

A <a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a> value that indicates the IP version of the inbound IPsec traffic.


### -field inboundUdpEncapsulation

Optional <a href="https://msdn.microsoft.com/69cddec0-7311-4833-8b24-293ad714054e">IPSEC_V4_UDP_ENCAPSULATION0</a> structure that specifies the IPsec NAT Traversal (NATT) UDP encapsulation ports. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field rngCryptoModuleID

Not used. A <b>IPSEC_CRYPTO_MODULE_ID</b> is a <b>GUID</b> value.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

