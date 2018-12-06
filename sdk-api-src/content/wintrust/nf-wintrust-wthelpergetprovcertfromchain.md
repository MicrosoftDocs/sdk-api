---
UID: NF:wintrust.WTHelperGetProvCertFromChain
title: WTHelperGetProvCertFromChain function
author: windows-sdk-content
description: Retrieves a trust provider certificate from the certificate chain.
old-location: security\wthelpergetprovcertfromchain.htm
tech.root: seccrypto
ms.assetid: 047278fe-37d5-4fd6-8b36-9e28ead0cc5a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WTHelperGetProvCertFromChain, WTHelperGetProvCertFromChain function [Security], security.wthelpergetprovcertfromchain, wintrust/WTHelperGetProvCertFromChain
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wintrust.h
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WTHelperGetProvCertFromChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTHelperGetProvCertFromChain function


## -description


<p class="CCE_Message">[The <b>WTHelperGetProvCertFromChain</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology signature verification, use the .NET Framework.]

The  <b>WTHelperGetProvCertFromChain</b> function retrieves a trust provider certificate from the certificate chain.  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param pSgnr [in]

A pointer to a <a href="https://msdn.microsoft.com/39cf9a03-768d-4ae0-a19d-17652181dbe4">CRYPT_PROVIDER_SGNR</a> structure that represents the signers. This pointer is retrieved by the <a href="https://msdn.microsoft.com/8e1ebf82-73c2-445b-9964-6739f7c90c47">WTHelperGetProvSignerFromChain</a> function.


### -param idxCert [in]

The index of the certificate. The index is zero based.


## -returns



If the function succeeds, the function returns a pointer to a  <a href="https://msdn.microsoft.com/622e7a72-445a-4820-b236-1c90dad08351">CRYPT_PROVIDER_CERT</a> structure that represents the trust provider certificate.

If the function fails, it returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/8e1ebf82-73c2-445b-9964-6739f7c90c47">WTHelperGetProvSignerFromChain</a>
 

 

