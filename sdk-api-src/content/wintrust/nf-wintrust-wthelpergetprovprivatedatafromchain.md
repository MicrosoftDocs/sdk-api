---
UID: NF:wintrust.WTHelperGetProvPrivateDataFromChain
title: WTHelperGetProvPrivateDataFromChain function
author: windows-sdk-content
description: Receives a CRYPT_PROVIDER_PRIVDATA structure from the chain by using the provider ID.
old-location: security\wthelpergetprovprivatedatafromchain.htm
old-project: SecCrypto
ms.assetid: 67a718a2-47ca-4c45-a939-99dd8311dc6d
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WTHelperGetProvPrivateDataFromChain, WTHelperGetProvPrivateDataFromChain function [Security], security.wthelpergetprovprivatedatafromchain, wintrust/WTHelperGetProvPrivateDataFromChain
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TEB, *PTEB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wintrust.dll
api_name:
-	WTHelperGetProvPrivateDataFromChain
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTHelperGetProvPrivateDataFromChain function


## -description


<p class="CCE_Message">[The <b>WTHelperGetProvPrivateDataFromChain</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperGetProvPrivateDataFromChain</b> function receives a <a href="https://msdn.microsoft.com/499e4d9b-991a-4317-bc74-a1dfb6609a70">CRYPT_PROVIDER_PRIVDATA</a> structure from the chain by using the provider ID. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param pProvData [in]

A pointer to a <a href="https://msdn.microsoft.com/93ea2ad5-65da-4daa-bfd4-e3d1307829b2">CRYPT_PROVIDER_DATA</a> structure that contains the provider's private information.


### -param pgProviderID

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that identifies the provider.


## -returns



If the function succeeds, the function returns a pointer to a  <a href="https://msdn.microsoft.com/499e4d9b-991a-4317-bc74-a1dfb6609a70">CRYPT_PROVIDER_PRIVDATA</a> structure that represents the trust provider's private information.

If the function fails, the return value is <b>NULL</b>.



