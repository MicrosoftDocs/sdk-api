---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_WRITE_CRL
title: PFN_CERT_STORE_PROV_WRITE_CRL
author: windows-sdk-content
description: An application-defined callback function that is called by CertAddEncodedCRLToStore, CertAddCRLContextToStore and CertAddSerializedElementToStore before adding to the store.
old-location: security\certstoreprovwritecrlcallback.htm
tech.root: SecCrypto
ms.assetid: ba259770-4462-4d1e-bd60-8572612fe032
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CertStoreProvWriteCRLCallback, PFN_CERT_STORE_PROV_WRITE_CRL, PFN_CERT_STORE_PROV_WRITE_CRL callback, PFN_CERT_STORE_PROV_WRITE_CRL callback function [Security], _crypto2_certstoreprovwritecrlcallback, security.certstoreprovwritecrlcallback, wincrypt/PFN_CERT_STORE_PROV_WRITE_CRL
ms.prod: windows
ms.technology: windows-sdk
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
 - PFN_CERT_STORE_PROV_WRITE_CRL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_WRITE_CRL callback function


## -description


An application-defined callback function that is called by 
<a href="https://msdn.microsoft.com/ec2361e6-a1e6-413a-828e-d543a09c88f8">CertAddEncodedCRLToStore</a>, 
<a href="https://msdn.microsoft.com/5dfa1c08-5d75-4ee4-bd65-ce56eb61ecce">CertAddCRLContextToStore</a> and 
<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a> before adding to the store. In addition to the encoded <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CRL</a>, the added <i>pCrlContext</i> might also have properties.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param pCrlContext [in]

See 
<a href="https://msdn.microsoft.com/5dfa1c08-5d75-4ee4-bd65-ce56eb61ecce">CertAddCRLContextToStore</a>.


### -param dwFlags [in]

CERT_STORE_PROV_WRITE_ADD_FLAG is used to specify when this function is called by the following functions that add a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CRL</a> to the store: 





<a href="https://msdn.microsoft.com/ec2361e6-a1e6-413a-828e-d543a09c88f8">CertAddEncodedCRLToStore</a>



<a href="https://msdn.microsoft.com/5dfa1c08-5d75-4ee4-bd65-ce56eb61ecce">CertAddCRLContextToStore</a>



<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a>



## -returns



Returns <b>TRUE</b> if it is okay to update the store.




## -see-also




<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Callback Functions</a>



<a href="https://msdn.microsoft.com/5dfa1c08-5d75-4ee4-bd65-ce56eb61ecce">CertAddCRLContextToStore</a>



<a href="https://msdn.microsoft.com/ec2361e6-a1e6-413a-828e-d543a09c88f8">CertAddEncodedCRLToStore</a>



<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a>



<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>
 

 

