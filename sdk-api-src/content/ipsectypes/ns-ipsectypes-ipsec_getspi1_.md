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

# IPSEC_GETSPI1_ structure


## -description


The <b>IPSEC_GETSPI1</b> structure contains information that must be supplied when requesting a security parameter index (SPI) from the IPsec driver.
<div class="alert"><b>Note</b>  <b>IPSEC_GETSPI1</b> is the specific implementation of IPSEC_GETSPI used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/a43c447c-83b4-4ca4-a7c5-7e10e6607692">IPSEC_GETSPI0</a> is available.</div><div> </div>

## -struct-fields




### -field inboundIpsecTraffic

An <a href="https://msdn.microsoft.com/2a3ad63f-9fa1-41c7-b628-5fe4e17ce7ac">IPSEC_TRAFFIC1</a> structure that describes traffic characteristics of the inbound IPsec SA.


### -field ipVersion

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a> value that indicates the IP version of the inbound IPsec traffic.


### -field inboundUdpEncapsulation

Optional <a href="https://msdn.microsoft.com/69cddec0-7311-4833-8b24-293ad714054e">IPSEC_V4_UDP_ENCAPSULATION0</a> structure that specifies the IPsec NAT Traversal (NATT) UDP encapsulation ports. 

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field rngCryptoModuleID

Not used. An <b>IPSEC_CRYPTO_MODULE_ID</b> is a <b>GUID</b> value.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

