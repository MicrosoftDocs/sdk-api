---
UID: NF:wincrypt.CertVerifyTimeValidity
title: CertVerifyTimeValidity function
author: windows-sdk-content
description: The CertVerifyTimeValidity function verifies the time validity of a certificate.
old-location: security\certverifytimevalidity.htm
tech.root: seccrypto
ms.assetid: 9ccf9230-e998-4f82-9db0-6cbaa1c36850
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CertVerifyTimeValidity, CertVerifyTimeValidity function [Security], _crypto2_certverifytimevalidity, security.certverifytimevalidity, wincrypt/CertVerifyTimeValidity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CertVerifyTimeValidity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertVerifyTimeValidity function


## -description


The <b>CertVerifyTimeValidity</b> function verifies the time validity of a certificate.


## -parameters




### -param pTimeToVerify [in]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the comparison time. If <b>NULL</b>, the current time is used.


### -param pCertInfo [in]

A pointer to the 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure of the certificate for which the time is being verified.


## -returns



Returns a minus one if the comparison time is before the <b>NotBefore</b> member of the 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure. Returns a plus one if the comparison time is after the <b>NotAfter</b> member. Returns zero for valid time for the certificate.
					




## -see-also




<a href="https://msdn.microsoft.com/a46ac5b5-bc44-4857-a7fb-4f35d438e3f7">CertVerifyCRLRevocation</a>



<a href="https://msdn.microsoft.com/ff321fe8-df45-4a1d-b626-055fb0696438">CertVerifyCRLTimeValidity</a>



<a href="https://msdn.microsoft.com/dc73a21d-5b55-45c4-80d2-220508d9f762">CertVerifyValidityNesting</a>



<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

