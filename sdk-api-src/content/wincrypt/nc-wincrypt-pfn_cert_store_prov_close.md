---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_CLOSE
title: PFN_CERT_STORE_PROV_CLOSE (wincrypt.h)
author: windows-sdk-content
description: An application-defined callback function that is called by CertCloseStore when the store's reference count is decremented to zero.
old-location: security\certstoreprovclosecallback.htm
tech.root: SecCrypto
ms.assetid: 2d0aa2c2-e79f-485c-ad47-6d9672c778da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertStoreProvCloseCallback, PFN_CERT_STORE_PROV_CLOSE, PFN_CERT_STORE_PROV_CLOSE callback, PFN_CERT_STORE_PROV_CLOSE callback function [Security], _crypto2_certstoreprovclosecallback, security.certstoreprovclosecallback, wincrypt/PFN_CERT_STORE_PROV_CLOSE
ms.topic: callback
f1_keywords:
- wincrypt/PFN_CERT_STORE_PROV_CLOSE
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
- PFN_CERT_STORE_PROV_CLOSE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFN_CERT_STORE_PROV_CLOSE callback function


## -description


An application-defined callback function that is called by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> when the store's <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a> is decremented to zero.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.


### -param dwFlags [in]

Copy of the <i>dwFlags</i> passed as a parameter to 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>.


## -returns



This callback function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>
 

 

