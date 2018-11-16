---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_DELETE_CERT
title: PFN_CERT_STORE_PROV_DELETE_CERT
author: windows-sdk-content
description: An application-defined callback function that is called by CertDeleteCertificateFromStore before deleting a certificate from the store.
old-location: security\certstoreprovdeletecertcallback.htm
tech.root: SecCrypto
ms.assetid: 0ae64bbc-05f6-4fc2-a05d-895654b4b97d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CertStoreProvDeleteCertCallback, PFN_CERT_STORE_PROV_DELETE_CERT, PFN_CERT_STORE_PROV_DELETE_CERT callback, PFN_CERT_STORE_PROV_DELETE_CERT callback function [Security], _crypto2_certstoreprovdeletecertcallback, security.certstoreprovdeletecertcallback, wincrypt/PFN_CERT_STORE_PROV_DELETE_CERT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_STORE_PROV_DELETE_CERT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_DELETE_CERT callback function


## -description


An application-defined callback function that is called by 
<a href="https://msdn.microsoft.com/4390c8da-9c4d-47a4-9af4-d179829f77f3">CertDeleteCertificateFromStore</a> before deleting a certificate from the store.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param pCertContext [in]

A pointer to the certificate context to be deleted.


### -param dwFlags [in]

Reserved for future use and is set to zero.


## -returns



Returns <b>TRUE</b> if it is okay to delete the certificate from the store. Otherwise, returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Callback Functions</a>
 

 

