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

# PstValidate function


## -description


Validates the specified certificate.


## -parameters




### -param pTargetName [in, optional]

The name of the server. If the caller is not the client, this parameter is <b>NULL</b>.


### -param bIsClient [in]

<b>TRUE</b> if the caller is the client; otherwise, <b>FALSE</b>.


### -param pRequestedIssuancePolicy [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/6154f1f7-4293-4b8e-91ab-9f57bb6f5743">CERT_USAGE_MATCH</a> structure that specifies identifiers that the certificate must match to be validated.


### -param phAdditionalCertStore [in, optional]

A handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> that contains additional certificates used for the authentication.


### -param pCert [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that specifies the certificate to validate.


### -param pProvGUID [out, optional]

A pointer to  a <b>GUID</b> structure that receives the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP) used for the authentication.


## -returns



If the function succeeds, return <b>STATUS_SUCCESS</b>.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.



