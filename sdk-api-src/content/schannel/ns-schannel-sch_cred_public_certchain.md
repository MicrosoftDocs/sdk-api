---
UID: NS:schannel._SCH_CRED_PUBLIC_CERTCHAIN
title: SCH_CRED_PUBLIC_CERTCHAIN (schannel.h)
description: The SCH_CRED_PUBLIC_CERTCHAIN structure contains a single certificate. A certification chain can be built from this certificate.
old-location: security\sch_cred_public_certchain.htm
tech.root: SecAuthN
ms.assetid: b6019f43-df94-4d30-9acf-a94772901e6e
ms.date: 12/05/2018
ms.keywords: '*PSCH_CRED_PUBLIC_CERTCHAIN, PSCH_CRED_PUBLIC_CERTCHAIN, PSCH_CRED_PUBLIC_CERTCHAIN structure pointer [Security], SCH_CRED_PUBLIC_CERTCHAIN, SCH_CRED_PUBLIC_CERTCHAIN structure [Security], _ssp_sch_cred_public_certchain, schannel/PSCH_CRED_PUBLIC_CERTCHAIN, schannel/SCH_CRED_PUBLIC_CERTCHAIN, security.sch_cred_public_certchain'
ms.topic: struct
f1_keywords:
- schannel/SCH_CRED_PUBLIC_CERTCHAIN
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Schannel.h
api_name:
- SCH_CRED_PUBLIC_CERTCHAIN
targetos: Windows
req.typenames: SCH_CRED_PUBLIC_CERTCHAIN, *PSCH_CRED_PUBLIC_CERTCHAIN
req.redist: 
ms.custom: 19H1
---

# SCH_CRED_PUBLIC_CERTCHAIN structure


## -description


<p class="CCE_Message">[The <b>SCH_CRED_PUBLIC_CERTCHAIN</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/schannel/ns-schannel-schannel_cred">SCHANNEL_CRED</a> structure.]

The <b>SCH_CRED_PUBLIC_CERTCHAIN</b> structure contains a single certificate. A certification chain can be built from this certificate.


## -struct-fields




### -field dwType

Must always be set to SCH_CRED_X509_CERTCHAIN.


### -field cbCertChain

Size of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/x-gly">X.509</a> certificate, in bytes.


### -field pCertChain

Pointer to an X.509 leaf certificate.


## -remarks



This structure does not directly support certificate chains. If a server needs to use certificate chains, the intermediate certificates can be placed in the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority's</a> (CA) <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate store</a> and Schannel will automatically pick them up from there.



