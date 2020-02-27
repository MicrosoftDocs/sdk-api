---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_WRITE_CRL
title: PFN_CERT_STORE_PROV_WRITE_CRL (wincrypt.h)
description: An application-defined callback function that is called by CertAddEncodedCRLToStore, CertAddCRLContextToStore and CertAddSerializedElementToStore before adding to the store.
old-location: security\certstoreprovwritecrlcallback.htm
tech.root: SecCrypto
ms.assetid: ba259770-4462-4d1e-bd60-8572612fe032
ms.date: 12/05/2018
ms.keywords: CertStoreProvWriteCRLCallback, PFN_CERT_STORE_PROV_WRITE_CRL, PFN_CERT_STORE_PROV_WRITE_CRL callback, PFN_CERT_STORE_PROV_WRITE_CRL callback function [Security], _crypto2_certstoreprovwritecrlcallback, security.certstoreprovwritecrlcallback, wincrypt/PFN_CERT_STORE_PROV_WRITE_CRL
f1_keywords:
- wincrypt/PFN_CERT_STORE_PROV_WRITE_CRL
dev_langs:
- c++
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
- PFN_CERT_STORE_PROV_WRITE_CRL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFN_CERT_STORE_PROV_WRITE_CRL callback function


## -description


An application-defined callback function that is called by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcrltostore">CertAddEncodedCRLToStore</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddserializedelementtostore">CertAddSerializedElementToStore</a> before adding to the store. In addition to the encoded <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">CRL</a>, the added <i>pCrlContext</i> might also have properties.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.


### -param pCrlContext [in]

See 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a>.


### -param dwFlags [in]

CERT_STORE_PROV_WRITE_ADD_FLAG is used to specify when this function is called by the following functions that add a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">CRL</a> to the store: 





<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcrltostore">CertAddEncodedCRLToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddserializedelementtostore">CertAddSerializedElementToStore</a>



## -returns



Returns <b>TRUE</b> if it is okay to update the store.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcrltostore">CertAddEncodedCRLToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddserializedelementtostore">CertAddSerializedElementToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>
 

 

