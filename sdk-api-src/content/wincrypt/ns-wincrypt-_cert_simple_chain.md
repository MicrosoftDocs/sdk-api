---
UID: NS:wincrypt._CERT_SIMPLE_CHAIN
title: "_CERT_SIMPLE_CHAIN"
author: windows-sdk-content
description: The CERT_SIMPLE_CHAIN structure contains an array of chain elements and a summary trust status for the chain that the array represents.
old-location: security\cert_simple_chain.htm
tech.root: seccrypto
ms.assetid: c130cab4-bf8d-429a-beb7-04cb5d37d466
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "*PCERT_SIMPLE_CHAIN, CERT_SIMPLE_CHAIN, CERT_SIMPLE_CHAIN structure [Security], PCERT_SIMPLE_CHAIN, PCERT_SIMPLE_CHAIN structure pointer [Security], _CERT_SIMPLE_CHAIN, _crypto2_cert_simple_chain, security.cert_simple_chain, wincrypt/CERT_SIMPLE_CHAIN, wincrypt/PCERT_SIMPLE_CHAIN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
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
 - Wincrypt.h
api_name:
 - CERT_SIMPLE_CHAIN
product: Windows
targetos: Windows
req.typenames: CERT_SIMPLE_CHAIN, *PCERT_SIMPLE_CHAIN
req.redist: 
---

# _CERT_SIMPLE_CHAIN structure


## -description


The <b>CERT_SIMPLE_CHAIN</b> structure contains an array of chain elements and a summary trust status for the chain that the array represents.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field TrustStatus

A structure that indicates the trust status of the whole chain. The structure includes an error status code and an information status code. For information about status code values, see <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a>.


### -field cElement

The number of <a href="https://msdn.microsoft.com/a1f6ba18-63ef-43ac-a17f-900fa13398aa">CERT_CHAIN_ELEMENT</a> structures in the array.


### -field rgpElement

An array of pointers to <a href="https://msdn.microsoft.com/a1f6ba18-63ef-43ac-a17f-900fa13398aa">CERT_CHAIN_ELEMENT</a> structures. <b>rgpElement</b>[0] is the end certificate chain element. <b>rgpElement</b>[<b>cElement</b>–1] is the self-signed "root" certificate element.


### -field pTrustListInfo

A pointer to a <a href="https://msdn.microsoft.com/774f5626-9b48-4585-b713-adbf191861cc">CERT_TRUST_LIST_INFO</a> structure that contains a pointer to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) connecting this chain to a next certificate chain. If the current chain is the final chain, <b>pTrustListInfo</b> is <b>NULL</b>.


### -field fHasRevocationFreshnessTime

BOOL. If <b>TRUE</b>, <b>dwRevocationFreshnessTime</b> has been calculated.


### -field dwRevocationFreshnessTime

The age of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> 
(CRL) in seconds, calculated as the CurrentTime minus the CRL's ThisUpdate time. This values is the largest time across all elements checked.


## -see-also




<a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a>



<a href="https://msdn.microsoft.com/a1f6ba18-63ef-43ac-a17f-900fa13398aa">CERT_CHAIN_ELEMENT</a>



<a href="https://msdn.microsoft.com/774f5626-9b48-4585-b713-adbf191861cc">CERT_TRUST_LIST_INFO</a>



<a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a>
 

 

