---
UID: NS:iketypes.IKEEXT_IPV6_CGA_AUTHENTICATION0_
title: IKEEXT_IPV6_CGA_AUTHENTICATION0_
author: windows-driver-content
description: Is used to specify various parameters for IPV6 cryptographically generated address (CGA) authentication.
old-location: fwp\ikeext_ipv6_cga_authentication0.htm
old-project: FWP
ms.assetid: 6b472140-f3e3-45b9-81f3-9c428b687fe4
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IKEEXT_IPV6_CGA_AUTHENTICATION0, IKEEXT_IPV6_CGA_AUTHENTICATION0 structure [Filtering], IKEEXT_IPV6_CGA_AUTHENTICATION0_, fwp.ikeext_ipv6_cga_authentication0, iketypes/IKEEXT_IPV6_CGA_AUTHENTICATION0
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IKEEXT_IPV6_CGA_AUTHENTICATION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_IPV6_CGA_AUTHENTICATION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_IPV6_CGA_AUTHENTICATION0_ structure


## -description


The <b>IKEEXT_IPV6_CGA_AUTHENTICATION0</b> structure is used to specify various parameters for IPV6 cryptographically generated address (CGA) authentication.


## -struct-fields




### -field keyContainerName

Key container name of the public key/private key pair that was used to generate the CGA.

Same semantics as the <b>pwszContainerName</b> member of the <a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure.


### -field cspName

Name of the CSP that stores the key container. If <b>NULL</b>, default provider will be used.

Same semantics as the <b>pwszProvName</b> member of the <a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure.


### -field cspType

Type of the CSP that stores the key container.

Same semantics as the <b>dwProvType</b> member of the <a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure.


### -field cgaModifier

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a> structure containing a modifier used during CGA generation.

See CGA RFC for more information.


### -field cgaCollisionCount

Collision count used during CGA generation.

See CGA RFC for more information.


## -remarks



<b>IKEEXT_IPV6_CGA_AUTHENTICATION0</b> is a specific implementation of IKEEXT_IPV6_CGA_AUTHENTICATION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

