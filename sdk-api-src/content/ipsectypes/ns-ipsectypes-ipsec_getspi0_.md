---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPSEC_GETSPI0_ structure


## -description


The <b>IPSEC_GETSPI0</b> structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.
<div class="alert"><b>Note</b>  <b>IPSEC_GETSPI0</b> is the specific implementation of IPSEC_GETSPI used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/671a8dd2-b4f6-4bdd-a6f1-1bf4260c6cbe">IPSEC_GETSPI1</a> is available.</div><div> </div>

## -struct-fields




### -field inboundIpsecTraffic

An <a href="https://msdn.microsoft.com/5be2da29-73d6-4381-8bde-3a3945ea7b5a">IPSEC_TRAFFIC0</a> structure that describes traffic characteristics of the inbound IPsec SA.


### -field ipVersion

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a> value that indicates the IP version of the inbound IPsec traffic.


### -field inboundUdpEncapsulation

Optional <a href="https://msdn.microsoft.com/69cddec0-7311-4833-8b24-293ad714054e">IPSEC_V4_UDP_ENCAPSULATION0</a> structure that specifies the IPsec NAT Traversal (NATT) UDP encapsulation ports. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field rngCryptoModuleID

Not used. A <b>IPSEC_CRYPTO_MODULE_ID</b> is a <b>GUID</b> value.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

