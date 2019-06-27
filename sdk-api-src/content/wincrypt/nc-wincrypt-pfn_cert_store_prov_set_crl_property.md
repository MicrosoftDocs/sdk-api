---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_SET_CRL_PROPERTY
title: PFN_CERT_STORE_PROV_SET_CRL_PROPERTY (wincrypt.h)
author: windows-sdk-content
description: An application-defined callback function that is called by CertSetCRLContextProperty before setting the CRL's property.
old-location: security\certstoreprovsetcrlpropertycallback.htm
tech.root: SecCrypto
ms.assetid: 98ad9b24-8d7d-4fbe-8fd8-089f1ddfbff0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertStoreProvSetCRLPropertyCallback, PFN_CERT_STORE_PROV_SET_CRL_PROPERTY, PFN_CERT_STORE_PROV_SET_CRL_PROPERTY callback, PFN_CERT_STORE_PROV_SET_CRL_PROPERTY callback function [Security], _crypto2_certstoreprovsetcrlpropertycallback, security.certstoreprovsetcrlpropertycallback, wincrypt/PFN_CERT_STORE_PROV_SET_CRL_PROPERTY
ms.topic: callback
f1_keywords: 
 - "wincrypt/PFN_CERT_STORE_PROV_SET_CRL_PROPERTY"
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
 - PFN_CERT_STORE_PROV_SET_CRL_PROPERTY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFN_CERT_STORE_PROV_SET_CRL_PROPERTY callback function


## -description


An application-defined callback function that is called by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a> before setting the CRL's property. It is also called by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a> when getting a hash property that needs to be created and then persisted through the set.

Upon input, the property has not been set for the <i>pCrlContext</i> parameter.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.


### -param pCrlContext [in]

See 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>.


### -param dwPropId [in]

See <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>.


### -param dwFlags [in]

Copy of the <i>dwFlags</i> passed as a parameter to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>.


### -param *pvData [in]

See <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>.


## -returns



Returns <b>TRUE</b> if it is okay to set the property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_store_prov_info">CERT_STORE_PROV_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>
 

 

