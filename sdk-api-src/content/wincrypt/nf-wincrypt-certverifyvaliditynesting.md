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
 

 

