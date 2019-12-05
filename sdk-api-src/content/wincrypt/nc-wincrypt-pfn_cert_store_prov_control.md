---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_CONTROL
title: PFN_CERT_STORE_PROV_CONTROL (wincrypt.h)
description: The CertStoreProvControl callback function supports the CertControlStore API. All of the API's parameters are passed straight through to the callback. For details, see CertControlStore.
old-location: security\certstoreprovcontrol.htm
tech.root: SecCrypto
ms.assetid: 0725d562-d04c-4fde-97f4-a294290266ee
ms.date: 12/05/2018
ms.keywords: CertStoreProvControl, CertStoreProvControl callback function [Security], PFN_CERT_STORE_PROV_CONTROL, PFN_CERT_STORE_PROV_CONTROL callback, _crypto2_certstoreprovcontrol, security.certstoreprovcontrol, wincrypt/CertStoreProvControl
ms.topic: callback
f1_keywords:
- wincrypt/CertStoreProvControl
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
- CertStoreProvControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFN_CERT_STORE_PROV_CONTROL callback function


## -description


The <b>CertStoreProvControl</b> callback function supports the <b>CertControlStore</b> API. All of the API's parameters are passed straight through to the callback. For details, see 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcontrolstore">CertControlStore</a>.


## -parameters




### -param hStoreProv [in, out]

<b>HCERTSTOREPROV</b> handle to a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate store</a> passed from the call to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcontrolstore">CertControlStore</a>.


### -param dwFlags [in]

Passed from the call to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcontrolstore">CertControlStore</a>.


### -param dwCtrlType [in]

Control action to be taken. Passed from the call to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcontrolstore">CertControlStore</a>.


### -param *pvCtrlPara [in, optional]

A pointer to a buffer whose structure and content is determined by the values of <i>dwFlags</i> and <i>dwCtrlType</i>. Passed from the call to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcontrolstore">CertControlStore</a>.


## -returns



Returns <b>TRUE</b> if the function succeeds or <b>FALSE</b> if it fails.



