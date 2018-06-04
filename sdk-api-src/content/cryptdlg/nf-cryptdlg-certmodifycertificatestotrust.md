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

# CertModifyCertificatesToTrust function


## -description


The <b>CertModifyCertificatesToTrust</b> function  modifies the set of certificates in a certificate trust list (CTL) for a given purpose.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters




### -param cCerts [in]

The number of modification requests that are in the <i>rgCerts</i> parameter.


### -param rgCerts [in]

A pointer to a <a href="https://msdn.microsoft.com/b8b5fd3e-a0db-4edd-84c7-48bae9adc3f8">CTL_MODIFY_REQUEST</a> structure that contains an array of modification requests.


### -param szPurpose [in]

A pointer to a null-terminated string that contains the string representation of an object identifier (OID). The OID specifies the enhanced key usage (EKU) of the CTL to be modified.


### -param hwnd [in]

A handle to the parent window of the dialog boxes that this function generates.


### -param hcertstoreTrust [in, optional]

A handle to the certificate store in which to modify the list of trusted certificates.  If <b>NULL</b>, the Trusted People store is used with the Current User location.


### -param pccertSigner [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains a certificate. It is used to sign the trust list. The certificate also restricts the set of trust lists that may be modified. If <b>NULL</b>, the trust list is not signed.


## -returns



An <b>HRESULT</b>. A value of S_OK indicates success.




## -see-also




<a href="https://msdn.microsoft.com/b8b5fd3e-a0db-4edd-84c7-48bae9adc3f8">CTL_MODIFY_REQUEST</a>
 

 

