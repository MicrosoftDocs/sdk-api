---
UID: NS:ipsectypes.IPSEC_DOSP_STATE_ENUM_TEMPLATE0_
title: IPSEC_DOSP_STATE_ENUM_TEMPLATE0 (ipsectypes.h)
author: windows-sdk-content
description: The IPSEC_DOSP_STATE_ENUM_TEMPLATE0 structure.
old-location: fwp\ipsec_dosp_state_enum_template0.htm
tech.root: fwp
ms.assetid: bfc34949-dd80-4fcd-8147-2fed62bce387
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_DOSP_STATE_ENUM_TEMPLATE0, IPSEC_DOSP_STATE_ENUM_TEMPLATE0 structure [Filtering], fwp.ipsec_dosp_state_enum_template0, ipsectypes/IPSEC_DOSP_STATE_ENUM_TEMPLATE0
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_DOSP_STATE_ENUM_TEMPLATE0
product: Windows
targetos: Windows
req.typenames: IPSEC_DOSP_STATE_ENUM_TEMPLATE0
req.redist: 
---

# IPSEC_DOSP_STATE_ENUM_TEMPLATE0 structure


## -description


The <b>IPSEC_DOSP_STATE_ENUM_TEMPLATE0</b> structure is used to enumerate IPsec DoS Protection state entries.


## -struct-fields




### -field publicV6AddrMask

An <a href="https://msdn.microsoft.com/d8566d41-677a-424f-89f3-e333a0520288">FWP_V6_ADDR_AND_MASK</a> structure that specifies the public IPv6 address.


### -field internalV6AddrMask

An <a href="https://msdn.microsoft.com/d8566d41-677a-424f-89f3-e333a0520288">FWP_V6_ADDR_AND_MASK</a> structure that specifies the internal IPv6 address.


## -remarks



<b>IPSEC_DOSP_STATE_ENUM_TEMPLATE0</b> is a specific implementation of IPSEC_DOSP_STATE_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/d8566d41-677a-424f-89f3-e333a0520288">FWP_V6_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

