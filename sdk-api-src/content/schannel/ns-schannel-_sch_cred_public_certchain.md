---
UID: NS:schannel._SCH_CRED_PUBLIC_CERTCHAIN
title: "_SCH_CRED_PUBLIC_CERTCHAIN"
author: windows-driver-content
description: The SCH_CRED_PUBLIC_CERTCHAIN structure contains a single certificate. A certification chain can be built from this certificate.
old-location: security\sch_cred_public_certchain.htm
old-project: SecAuthN
ms.assetid: b6019f43-df94-4d30-9acf-a94772901e6e
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PSCH_CRED_PUBLIC_CERTCHAIN, PSCH_CRED_PUBLIC_CERTCHAIN, PSCH_CRED_PUBLIC_CERTCHAIN structure pointer [Security], SCH_CRED_PUBLIC_CERTCHAIN, SCH_CRED_PUBLIC_CERTCHAIN structure [Security], _SCH_CRED_PUBLIC_CERTCHAIN, _ssp_sch_cred_public_certchain, schannel/PSCH_CRED_PUBLIC_CERTCHAIN, schannel/SCH_CRED_PUBLIC_CERTCHAIN, security.sch_cred_public_certchain"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: schannel.h
req.include-header: Schnlsp.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SCH_CRED_PUBLIC_CERTCHAIN, *PSCH_CRED_PUBLIC_CERTCHAIN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Schannel.h
api_name:
-	SCH_CRED_PUBLIC_CERTCHAIN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SCH_CRED_PUBLIC_CERTCHAIN structure


## -description


<p class="CCE_Message">[The <b>SCH_CRED_PUBLIC_CERTCHAIN</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/8398e029-473e-488f-a861-c7ceae07e678">SCHANNEL_CRED</a> structure.]


			The <b>SCH_CRED_PUBLIC_CERTCHAIN</b> structure contains a single certificate. A certification chain can be built from this certificate.


## -struct-fields




### -field dwType

Must always be set to SCH_CRED_X509_CERTCHAIN.


### -field cbCertChain

Size of the <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate, in bytes.


### -field pCertChain

Pointer to an X.509 leaf certificate.


## -remarks



This structure does not directly support certificate chains. If a server needs to use certificate chains, the intermediate certificates can be placed in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority's</a> (CA) <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> and Schannel will automatically pick them up from there.



