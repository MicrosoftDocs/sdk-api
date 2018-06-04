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

# _CERT_SELECT_CHAIN_PARA structure


## -description


The <b>CERT_SELECT_CHAIN_PARA</b> structure contains the parameters used for building and selecting chains. This structure is used by the   <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a> functions.


## -struct-fields




### -field hChainEngine

The handle of the chain engine to use to build the chain. If the value of the <i>hChainEngine</i> parameter is <b>NULL</b>, the default chain engine, <b>HCCE_CURRENT_USER</b>, is used.


### -field pTime

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time for which the chain is to be validated. If the  value of the <i>pTime</i> parameter is <b>NULL</b>, the current system time is passed to this parameter. 

<div class="alert"><b>Note</b>  The time does not affect trust list, revocation, or root store checking.</div>
<div> </div>

### -field hAdditionalStore

The handle of any additional store to search for supporting certificates and certificate trust lists (CTLs). This parameter can be <b>NULL</b> if no additional store is to be searched. 


### -field pChainPara

A pointer to a <a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a> structure that includes chain-building parameters. 


### -field dwFlags

Flag values that indicate special processing during chain build. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY"></a><a id="cert_chain_revocation_check_cache_only"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Revocation checking only accesses cached URLs.


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL"></a><a id="cert_chain_cache_only_url_retrieval"></a><dl>
<dt><b>CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Use only cached URLs in building a certificate chain. The Internet and intranet are not searched for URL-based objects.


</td>
</tr>
</table>
 


## -remarks



Trust in a particular certificate being a trusted root is based on the current state of the root store and not the state of the root store at a time passed in by this parameter. For revocation, a certificate revocation list (CRL), itself, must be valid at the current time. The value of this parameter is used to determine whether a certificate listed in a CRL has been revoked.

The following remarks apply to strong signature checking:

<ul>
<li>You can enable strong signature checking by using the <a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a> structure referenced by the <b>pChainPara</b> member. The <b>pStrongSignPara</b> member of the <b>CERT_CHAIN_PARA</b> structure points to a <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure that can be used to determine signature strength.</li>
<li>When you enable strong checking and a weak signature is encountered, the <b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b> and <b>CERT_TRUST_HAS_WEAK_SIGNATURE</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure.</li>
</ul>


