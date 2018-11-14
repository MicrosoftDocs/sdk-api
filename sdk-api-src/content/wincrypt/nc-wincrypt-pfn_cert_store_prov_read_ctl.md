---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_READ_CTL
title: PFN_CERT_STORE_PROV_READ_CTL
author: windows-sdk-content
description: The CertStoreProvReadCTL callback function is called to read the provider's copy of the CTL context and, if it exists, to create a new CTL context.
old-location: security\certstoreprovreadctl.htm
tech.root: seccrypto
ms.assetid: 09fbf42d-ed7a-4b1d-bad6-3bf8f216603c
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CertStoreProvReadCTL, PFN_CERT_STORE_PROV_READ_CTL, PFN_CERT_STORE_PROV_READ_CTL callback, PFN_CERT_STORE_PROV_READ_CTL callback function [Security], _crypto2_certstoreprovreadctl, security.certstoreprovreadctl, wincrypt/PFN_CERT_STORE_PROV_READ_CTL
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
 - PFN_CERT_STORE_PROV_READ_CTL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_READ_CTL callback function


## -description


The <b>CertStoreProvReadCTL</b> callback function is called to read the provider's copy of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTL</a> context and, if it exists, to create a new CTL context. Currently, this callback function is not called directly by the store APIs but it can be exported to support other providers based on it.


## -parameters




### -param hStoreProv [in]

<b>HCERTSTOREPROV</b> handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


### -param pStoreCtlContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure.


### -param dwFlags [in]

Any needed flag values.


### -param *ppProvCtlContext [out]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure to be returned by the function. The context will be freed by calling <a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>.


## -returns



Returns <b>TRUE</b> if the function succeeds or <b>FALSE</b> if it fails.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>
 

 

