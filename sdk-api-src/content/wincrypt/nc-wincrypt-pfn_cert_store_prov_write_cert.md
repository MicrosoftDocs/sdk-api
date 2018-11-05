---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_WRITE_CERT
title: PFN_CERT_STORE_PROV_WRITE_CERT
author: windows-sdk-content
description: An application-defined callback function that is called by CertAddEncodedCertificateToStore, CertAddCertificateContextToStore and CertAddSerializedElementToStore before adding to the store.
old-location: security\certstoreprovwritecertcallback.htm
tech.root: seccrypto
ms.assetid: 97cc488a-7993-4b48-a4b4-cb13c6168226
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CertStoreProvWriteCertCallback, PFN_CERT_STORE_PROV_WRITE_CERT, PFN_CERT_STORE_PROV_WRITE_CERT callback, PFN_CERT_STORE_PROV_WRITE_CERT callback function [Security], _crypto2_certstoreprovwritecertcallback, security.certstoreprovwritecertcallback, wincrypt/PFN_CERT_STORE_PROV_WRITE_CERT
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
 - PFN_CERT_STORE_PROV_WRITE_CERT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_WRITE_CERT callback function


## -description


An application-defined callback function that is called by 
<a href="https://msdn.microsoft.com/7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d">CertAddEncodedCertificateToStore</a>, 
<a href="https://msdn.microsoft.com/5e4d8cae-1096-491f-9a04-92b7e9c020bb">CertAddCertificateContextToStore</a> and 
<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a> before adding to the store. In addition to the encoded certificate, the added <i>pCertContext</i> might also have properties.


## -parameters




### -param hStoreProv [in]

Provider specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param pCertContext [in]

See 
<a href="https://msdn.microsoft.com/5e4d8cae-1096-491f-9a04-92b7e9c020bb">CertAddCertificateContextToStore</a>.


### -param dwFlags [in]

CERT_STORE_PROV_WRITE_ADD_FLAG is set when this function is called by the following functions that add a certificate to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">store</a>: 





<a href="https://msdn.microsoft.com/7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d">CertAddEncodedCertificateToStore</a>



<a href="https://msdn.microsoft.com/5e4d8cae-1096-491f-9a04-92b7e9c020bb">CertAddCertificateContextToStore</a>



<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a>



## -returns



Returns <b>TRUE</b> if it is okay to update the store.




## -see-also




<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Callback Functions</a>



<a href="https://msdn.microsoft.com/5e4d8cae-1096-491f-9a04-92b7e9c020bb">CertAddCertificateContextToStore</a>



<a href="https://msdn.microsoft.com/7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d">CertAddEncodedCertificateToStore</a>



<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a>



<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>
 

 

