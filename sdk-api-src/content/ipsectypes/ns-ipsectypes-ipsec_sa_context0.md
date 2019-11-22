---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT0_
title: IPSEC_SA_CONTEXT0 (ipsectypes.h)

description: Encapsulates an inbound and outbound SA pair.
old-location: fwp\ipsec_sa_context0.htm
tech.root: fwp
ms.assetid: 1cf191f0-5052-40f6-8665-747ae3f38fb1

ms.date: 12/05/2018
ms.keywords: IPSEC_SA_CONTEXT0, IPSEC_SA_CONTEXT0 structure [Filtering], fwp.ipsec_sa_context0, ipsectypes/IPSEC_SA_CONTEXT0
ms.topic: struct
f1_keywords: 
 - "ipsectypes/IPSEC_SA_CONTEXT0"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: IPSEC_SA_CONTEXT0
req.redist: 
ms.custom: 19H1
---

# IPSEC_SA_CONTEXT0 structure


## -description


The <b>IPSEC_SA_CONTEXT0</b> structure encapsulates an inbound and outbound SA pair.
<div class="alert"><b>Note</b>  <b>IPSEC_SA_CONTEXT0</b> is the specific implementation of IPSEC_SA_CONTEXT used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context1_">IPSEC_SA_CONTEXT1</a> is available.</div><div> </div>

## -struct-fields




### -field saContextId

Identifies the SA context.


### -field inboundSa

An <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details0_">IPSEC_SA_DETAILS0</a> structure that contains information about the inbound SA.


### -field outboundSa

An <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details0_">IPSEC_SA_DETAILS0</a> structure that contains information about the outbound SA.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

