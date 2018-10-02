---
UID: NS:ipsectypes.IPSEC_SA_LIFETIME0_
title: IPSEC_SA_LIFETIME0_
author: windows-sdk-content
description: Stores the lifetime in seconds/kilobytes/packets for an IPsec security association (SA).
old-location: fwp\ipsec_sa_lifetime0_struct.htm
tech.root: FWP
ms.assetid: 9ade5a9a-5c48-4a94-bb35-77f9866e8e6f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPSEC_SA_LIFETIME0, IPSEC_SA_LIFETIME0 structure [Filtering], IPSEC_SA_LIFETIME0_, fwp.ipsec_sa_lifetime0_struct, ipsectypes/IPSEC_SA_LIFETIME0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_SA_LIFETIME0
product: Windows
targetos: Windows
req.typenames: IPSEC_SA_LIFETIME0
req.redist: 
---

# IPSEC_SA_LIFETIME0_ structure


## -description


The <b>IPSEC_SA_LIFETIME0</b> structure stores the lifetime in seconds/kilobytes/packets for an IPsec security association (SA).


## -struct-fields




### -field lifetimeSeconds

SA lifetime in seconds.


### -field lifetimeKilobytes

SA lifetime in kilobytes.


### -field lifetimePackets

SA lifetime in packets.


## -remarks



<b>IPSEC_SA_LIFETIME0</b> is a specific implementation of IPSEC_SA_LIFETIME. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

