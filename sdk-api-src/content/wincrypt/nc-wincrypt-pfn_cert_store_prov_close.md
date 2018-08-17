---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_CLOSE
title: PFN_CERT_STORE_PROV_CLOSE
author: windows-sdk-content
description: An application-defined callback function that is called by CertCloseStore when the store's reference count is decremented to zero.
old-location: security\certstoreprovclosecallback.htm
old-project: SecCrypto
ms.assetid: 2d0aa2c2-e79f-485c-ad47-6d9672c778da
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CertStoreProvCloseCallback, CertStoreProvCloseCallback callback, CertStoreProvCloseCallback callback function [Security], PFN_CERT_STORE_PROV_CLOSE, PFN_CERT_STORE_PROV_CLOSE callback function [Security], _crypto2_certstoreprovclosecallback, security.certstoreprovclosecallback, wincrypt/CertStoreProvCloseCallback, wincrypt/PFN_CERT_STORE_PROV_CLOSE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - CertStoreProvCloseCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_CERT_STORE_PROV_CLOSE callback function


## -description


An application-defined callback function that is called by 
<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a> when the store's <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> is decremented to zero.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param dwFlags [in]

Copy of the <i>dwFlags</i> passed as a parameter to 
<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a>.


## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Callback Functions</a>
 

 

