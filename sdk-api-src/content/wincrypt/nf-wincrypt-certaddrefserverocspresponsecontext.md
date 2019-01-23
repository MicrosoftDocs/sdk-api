---
UID: NF:wincrypt.CertAddRefServerOcspResponseContext
title: CertAddRefServerOcspResponseContext function
author: windows-sdk-content
description: Increments the reference count for a CERT_SERVER_OCSP_RESPONSE_CONTEXT structure.
old-location: security\certaddrefserverocspresponsecontext.htm
tech.root: SecCrypto
ms.assetid: b7cdce9b-25fe-4fb9-b266-61989793699b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CertAddRefServerOcspResponseContext, CertAddRefServerOcspResponseContext function [Security], security.certaddrefserverocspresponsecontext, wincrypt/CertAddRefServerOcspResponseContext
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CertAddRefServerOcspResponseContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertAddRefServerOcspResponseContext function


## -description


The <b>CertAddRefServerOcspResponseContext</b> function increments the reference count for a <a href="https://msdn.microsoft.com/en-us/library/Bb540821(v=VS.85).aspx">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure.


## -parameters




### -param pServerOcspResponseContext [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb540821(v=VS.85).aspx">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> returned by <a href="https://msdn.microsoft.com/07476e43-db6b-4119-8d6b-41143b98744e">CertGetServerOcspResponseContext</a>.


## -returns



The function has no return value.




## -remarks



Each call to <a href="https://msdn.microsoft.com/07476e43-db6b-4119-8d6b-41143b98744e">CertGetServerOcspResponseContext</a> and <b>CertAddRefServerOcspResponseContext</b> requires a corresponding call to <a href="https://msdn.microsoft.com/a07fc1e0-6f06-4336-b33c-d4d6a838b609">CertFreeServerOcspResponseContext</a>.



