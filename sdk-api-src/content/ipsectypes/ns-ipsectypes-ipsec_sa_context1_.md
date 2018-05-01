---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT1_
title: IPSEC_SA_CONTEXT1_
author: windows-driver-content
description: Encapsulates an inbound and outbound security association (SA) pair.
old-location: fwp\ipsec_sa_context1.htm
old-project: FWP
ms.assetid: a3e210a7-cd3a-42fc-b3a0-7df9ad6778af
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: IPSEC_SA_CONTEXT1, IPSEC_SA_CONTEXT1 structure [Filtering], IPSEC_SA_CONTEXT1_, fwp.ipsec_sa_context1, ipsectypes/IPSEC_SA_CONTEXT1
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IPSEC_SA_CONTEXT1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_SA_CONTEXT1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_SA_CONTEXT1_ structure


## -description


The <b>IPSEC_SA_CONTEXT1</b> structure encapsulates an inbound and outbound security association (SA) pair.
<div class="alert"><b>Note</b>  <b>IPSEC_SA_CONTEXT1</b> is the specific implementation of IPSEC_SA_CONTEXT used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/1cf191f0-5052-40f6-8665-747ae3f38fb1">IPSEC_SA_CONTEXT0</a> is available.</div><div> </div>

## -struct-fields




### -field saContextId

Identifies the SA context.


### -field inboundSa

An <a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a> structure that contains information about the inbound SA.


### -field outboundSa

An <a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a> structure that contains information about the outbound SA.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

