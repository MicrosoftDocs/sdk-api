---
UID: NF:wintrust.WTHelperGetProvSignerFromChain
title: WTHelperGetProvSignerFromChain function
author: windows-sdk-content
description: Retrieves a signer or countersigner by index from the chain.
old-location: security\wthelpergetprovsignerfromchain.htm
tech.root: SecCrypto
ms.assetid: 8e1ebf82-73c2-445b-9964-6739f7c90c47
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WTHelperGetProvSignerFromChain, WTHelperGetProvSignerFromChain function [Security], security.wthelpergetprovsignerfromchain, wintrust/WTHelperGetProvSignerFromChain
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
 - WTHelperGetProvSignerFromChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WTHelperGetProvSignerFromChain
: 
---

# WTHelperGetProvSignerFromChain function


## -description


<p class="CCE_Message">[The <b>WTHelperGetProvSignerFromChain</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperGetProvSignerFromChain</b> function retrieves a  signer or countersigner by index from the chain.  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param pProvData [in]

A pointer to the <a href="https://msdn.microsoft.com/93ea2ad5-65da-4daa-bfd4-e3d1307829b2">CRYPT_PROVIDER_DATA</a> structure that contains the signer and countersigner information.


### -param idxSigner [in]

The index of the signer. The index is zero based.


### -param fCounterSigner [in]

If <b>TRUE</b>, the countersigner, as specified by <i>idxCounterSigner</i>, is retrieved by this function; the signer that contains the countersigner is identified by  <i>idxSigner</i>. If <b>FALSE</b>, the signer, as specified by <i>idxSigner</i>, is retrieved by this function.


### -param idxCounterSigner [in]

The index of the countersigner. The index is zero based. The countersigner applies to the signer identified by <i>idxSigner</i>.


## -returns



If the function succeeds, the function returns a pointer to a <a href="https://msdn.microsoft.com/39cf9a03-768d-4ae0-a19d-17652181dbe4">CRYPT_PROVIDER_SGNR</a> structure for the requested signer or countersigner.

If the function fails, it returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/047278fe-37d5-4fd6-8b36-9e28ead0cc5a">WTHelperGetProvCertFromChain</a>
 

 

