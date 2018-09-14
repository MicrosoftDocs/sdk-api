---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT0_
title: IPSEC_SA_CONTEXT0_
author: windows-sdk-content
description: Encapsulates an inbound and outbound SA pair.
old-location: fwp\ipsec_sa_context0.htm
tech.root: FWP
ms.assetid: 1cf191f0-5052-40f6-8665-747ae3f38fb1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPSEC_SA_CONTEXT0, IPSEC_SA_CONTEXT0 structure [Filtering], IPSEC_SA_CONTEXT0_, fwp.ipsec_sa_context0, ipsectypes/IPSEC_SA_CONTEXT0
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
 - IPSEC_SA_CONTEXT0
product: Windows
targetos: Windows
req.typenames: IPSEC_SA_CONTEXT0
req.redist: 
---

# IPSEC_SA_CONTEXT0_ structure


## -description


The <b>IPSEC_SA_CONTEXT0</b> structure encapsulates an inbound and outbound SA pair.
<div class="alert"><b>Note</b>  <b>IPSEC_SA_CONTEXT0</b> is the specific implementation of IPSEC_SA_CONTEXT used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/a3e210a7-cd3a-42fc-b3a0-7df9ad6778af">IPSEC_SA_CONTEXT1</a> is available.</div><div> </div>

## -struct-fields




### -field saContextId

Identifies the SA context.


### -field inboundSa

An <a href="https://msdn.microsoft.com/261cea6e-4a56-404f-9e5d-70ce95122f9f">IPSEC_SA_DETAILS0</a> structure that contains information about the inbound SA.


### -field outboundSa

An <a href="https://msdn.microsoft.com/261cea6e-4a56-404f-9e5d-70ce95122f9f">IPSEC_SA_DETAILS0</a> structure that contains information about the outbound SA.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

