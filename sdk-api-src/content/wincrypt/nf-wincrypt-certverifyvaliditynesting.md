---
UID: NF:wincrypt.CertVerifyValidityNesting
title: CertVerifyValidityNesting function
author: windows-sdk-content
description: The CertVerifyValidityNesting function verifies that a subject certificate's time validity nests correctly within its issuer's time validity.
old-location: security\certverifyvaliditynesting.htm
tech.root: seccrypto
ms.assetid: dc73a21d-5b55-45c4-80d2-220508d9f762
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CertVerifyValidityNesting, CertVerifyValidityNesting function [Security], _crypto2_certverifyvaliditynesting, security.certverifyvaliditynesting, wincrypt/CertVerifyValidityNesting
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertVerifyValidityNesting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertVerifyValidityNesting function


## -description


The <b>CertVerifyValidityNesting</b> function verifies that a subject certificate's time validity nests correctly within its issuer's time validity.


## -parameters




### -param pSubjectInfo [in]

A pointer to the 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure of the subject certificate.


### -param pIssuerInfo [in]

A pointer to the <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure of the issuer certificate.


## -returns



Returns <b>TRUE</b> if the <b>NotBefore</b> time of the subject's certificate is after the <b>NotBefore</b> time of the issuer's certificate and the <b>NotAfter</b> time of the subject's certificate is not after the <b>NotAfter</b> time of the issuer's certificate. Otherwise, returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a46ac5b5-bc44-4857-a7fb-4f35d438e3f7">CertVerifyCRLRevocation</a>



<a href="https://msdn.microsoft.com/ff321fe8-df45-4a1d-b626-055fb0696438">CertVerifyCRLTimeValidity</a>



<a href="https://msdn.microsoft.com/9ccf9230-e998-4f82-9db0-6cbaa1c36850">CertVerifyTimeValidity</a>



<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

