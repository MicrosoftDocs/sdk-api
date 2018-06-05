---
UID: NF:schannel.SslCrackCertificate
title: SslCrackCertificate function
author: windows-sdk-content
description: Returns an X509Certificate structure with the information contained in the specified certificate BLOB.
old-location: security\sslcrackcertificate.htm
old-project: SecAuthN
ms.assetid: e5ffeebb-0b09-4f0a-b2dc-75fb2a3af7ed
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SslCrackCertificate, SslCrackCertificate function [Security], schannel/SslCrackCertificate, security.sslcrackcertificate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: schannel.h
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
tech.root: 
req.typenames: SCESVC_CONFIGURATION_LINE, *PSCESVC_CONFIGURATION_LINE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Schannel.dll
api_name:
-	SslCrackCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: Schannel.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SslCrackCertificate function


## -description


<p class="CCE_Message">[The <b>SslCrackCertificate</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/a32714c4-ee88-48a8-a40a-bbbfec0613ac">CertCreateCertificateContext</a> function.]

Returns an <a href="https://msdn.microsoft.com/5a337f78-e5de-4ea2-9c15-1056d9e9e38c">X509Certificate</a> structure with the information contained in the specified certificate <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Schannel.dll.


## -parameters




### -param pbCertificate [in]

The certificate BLOB from which to create the new <a href="https://msdn.microsoft.com/5a337f78-e5de-4ea2-9c15-1056d9e9e38c">X509Certificate</a> structure.


### -param cbCertificate

TBD


### -param dwFlags [in]

Set this value to <b>CF_CERT_FROM_FILE</b> to specify that the certificate BLOB contained in the <i>pbCertificate</i> parameter is from a file.


### -param ppCertificate [out]

On return, receives the address of a pointer to the <a href="https://msdn.microsoft.com/5a337f78-e5de-4ea2-9c15-1056d9e9e38c">X509Certificate</a> structure that this function creates.

When you have finished using the <a href="https://msdn.microsoft.com/5a337f78-e5de-4ea2-9c15-1056d9e9e38c">X509Certificate</a> structure, free it by calling <a href="https://msdn.microsoft.com/bf643ece-fe79-4f6e-a216-108fce6757a4">SslFreeCertificate</a>.


#### - dwCertificate [in]

The length, in bytes, of the BLOB contained in the <i>pbCertificate</i> parameter.


## -returns



Returns nonzero if this function successfully created an <a href="https://msdn.microsoft.com/5a337f78-e5de-4ea2-9c15-1056d9e9e38c">X509Certificate</a> structure or zero otherwise. 



