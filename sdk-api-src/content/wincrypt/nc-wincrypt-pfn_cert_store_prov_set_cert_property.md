---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_SET_CERT_PROPERTY
title: PFN_CERT_STORE_PROV_SET_CERT_PROPERTY
author: windows-sdk-content
description: An application-defined callback function that is called by CertSetCertificateContextProperty before setting the certificate's property.
old-location: security\certstoreprovsetcertpropertycallback.htm
tech.root: SecCrypto
ms.assetid: 03d7e1f6-030f-4eae-b76d-5465748d9583
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CertStoreProvSetCertPropertyCallback, PFN_CERT_STORE_PROV_SET_CERT_PROPERTY, PFN_CERT_STORE_PROV_SET_CERT_PROPERTY callback function [Security], PFN_CERT_STORE_PROV_SET_CRL_PROPERTY, PFN_CERT_STORE_PROV_SET_CRL_PROPERTY callback, PFN_CERT_STORE_PROV_SET_CRL_PROPERTY callback function [Security], _crypto2_certstoreprovsetcertpropertycallback, security.certstoreprovsetcertpropertycallback, wincrypt/PFN_CERT_STORE_PROV_SET_CERT_PROPERTY, wincrypt/PFN_CERT_STORE_PROV_SET_CRL_PROPERTY
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
 - PFN_CERT_STORE_PROV_SET_CRL_PROPERTY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_SET_CERT_PROPERTY callback function


## -description


An application-defined callback function that is called by 
<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a> before setting the certificate's property. It is also called by 
<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a> when getting a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> property that needs to be created and then persisted through the set.

Upon input, the property has not been set for the <i>pCertContext</i> parameter.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param pCertContext [in]

See 
<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>.


### -param dwPropId [in]

See <a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>.


### -param dwFlags [in]

Copy of the <i>dwFlags</i> passed as a parameter to <a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>.


### -param *pvData [in]

See <a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>.


## -returns



Returns <b>TRUE</b> if it is okay to set the property.




## -see-also




<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Callback Functions</a>



<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>



<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a>



<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>
 

 

