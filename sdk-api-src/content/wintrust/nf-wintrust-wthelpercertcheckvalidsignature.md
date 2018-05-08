---
UID: NF:wintrust.WTHelperCertCheckValidSignature
title: WTHelperCertCheckValidSignature function
author: windows-driver-content
description: Checks whether a signature is valid.
old-location: security\wthelpercertcheckvalidsignature.htm
old-project: SecCrypto
ms.assetid: d46eea18-03cb-4199-873e-0e9e13061598
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: WTHelperCertCheckValidSignature, WTHelperCertCheckValidSignature function [Security], security.wthelpercertcheckvalidsignature, wintrust/WTHelperCertCheckValidSignature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
req.typenames: TEB, *PTEB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wintrust.dll
api_name:
-	WTHelperCertCheckValidSignature
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTHelperCertCheckValidSignature function


## -description


<p class="CCE_Message">[The <b>WTHelperCertCheckValidSignature</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperCertCheckValidSignature</b> function checks whether a signature is valid.  It can be used by trust providers to get an initial assessment of the validity of a signature before calling the function pointed to by the <b>pfnFinalPolicy</b> member of a <a href="https://msdn.microsoft.com/2c00f8ec-e262-4df8-8984-a2702a4162bf">CRYPT_PROVIDER_FUNCTIONS</a> structure.


## -parameters




### -param pProvData

A pointer to the <a href="https://msdn.microsoft.com/93ea2ad5-65da-4daa-bfd4-e3d1307829b2">CRYPT_PROVIDER_DATA</a> structure that contains the signer and countersigner information.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of possible error values, see <a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a>.



