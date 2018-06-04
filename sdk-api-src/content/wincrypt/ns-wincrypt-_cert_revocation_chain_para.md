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

# _CERT_REVOCATION_CHAIN_PARA structure


## -description


The <b>CERT_REVOCATION_CHAIN_PARA</b> structure contains parameters used for building a chain for an independent <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) response signer certificate. The <a href="https://msdn.microsoft.com/730db593-c55f-4ecf-bcac-5de54ab90db6">CERT_REVOCATION_PARA</a> and <a href="https://msdn.microsoft.com/3de595f9-c922-4c8f-8328-819e91a2997c">CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO</a> structure definitions include optional pointers to this structure.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hChainEngine

A handle to the chain engine used by the caller.


### -field hAdditionalStore

A handle to a store that contains the certificates used to build the original chain. The handle can be <b>NULL</b>.


### -field dwChainFlags

A value for the <i>dwFlags</i> parameter passed to the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT"></a><a id="cert_chain_revocation_check_ocsp_cert"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
This flag will be set by the <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> provider when it
calls <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> with an independent OCSP signer certificate.
When set, <b>CertGetCertificateChain</b> will call <b>CertVerifyRevocation</b> without
setting the pointer to the above <b>CERT_REVOCATION_CHAIN_PARA</b> data structure; this helps to prevent circular revocation checking.

</td>
</tr>
</table>
 


### -field dwUrlRetrievalTimeout

A value that contains the time-out limit, in milliseconds. If zero, the revocation handler's default time-out is used.


### -field pftCurrentTime

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure used in the freshness time check. If this pointer is <b>NULL</b>, the revocation handler uses the current time.


### -field pftCacheResync

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that governs the use of cached information. Any information cached  before this time is considered invalid and new information is retrieved. When set, this value overrides
    the registry configuration CacheResync time.


### -field cbMaxUrlRetrievalByteCount

A <b>DWORD</b> value that specifies the maximum number of bytes to download from the URL object. A value of 0 specifies no limit.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not supported.

