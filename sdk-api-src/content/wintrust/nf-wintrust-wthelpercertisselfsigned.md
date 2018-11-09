---
UID: NF:wintrust.WTHelperCertIsSelfSigned
title: WTHelperCertIsSelfSigned function
author: windows-sdk-content
description: Checks whether a certificate is self-signed.
old-location: security\wthelpercertisselfsigned.htm
tech.root: seccrypto
ms.assetid: 456b8c8c-6ca3-469a-a415-e72109696bf5
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: WTHelperCertIsSelfSigned, WTHelperCertIsSelfSigned function [Security], security.wthelpercertisselfsigned, wintrust/WTHelperCertIsSelfSigned
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
 - WTHelperCertIsSelfSigned
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTHelperCertIsSelfSigned function


## -description


<p class="CCE_Message">[The <b>WTHelperCertIsSelfSigned</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperCertIsSelfSigned</b> function checks whether a certificate is self-signed. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param dwEncoding [in]

A <b>DWORD</b> value that specifies the encoding types of the certificate to check. For information about possible encoding types, see <a href="https://msdn.microsoft.com/97b25435-aec2-4fdb-a4c6-89ec2e26f51d">Certificate and Message Encoding Types</a>.


### -param pCert [in]

A pointer to a <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure that contains information about  the certificate to check.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.



