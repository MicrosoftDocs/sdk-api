---
UID: NF:wincrypt.CertAddRefServerOcspResponse
title: CertAddRefServerOcspResponse function (wincrypt.h)
author: windows-sdk-content
description: Increments the reference count for an HCERT_SERVER_OCSP_RESPONSE handle.
old-location: security\certaddrefserverocspresponse.htm
tech.root: SecCrypto
ms.assetid: 6ccc0e85-1fa0-480c-a5b4-b21ba811e5d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertAddRefServerOcspResponse, CertAddRefServerOcspResponse function [Security], security.certaddrefserverocspresponse, wincrypt/CertAddRefServerOcspResponse
ms.topic: function
f1_keywords: 
 - "wincrypt/CertAddRefServerOcspResponse"
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertAddRefServerOcspResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertAddRefServerOcspResponse function


## -description


The <b>CertAddRefServerOcspResponse</b> function increments the reference count for an <b>HCERT_SERVER_OCSP_RESPONSE</b> handle.


## -parameters




### -param hServerOcspResponse [in]

A handle to an <b>HCERT_SERVER_OCSP_RESPONSE</b> returned by <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certopenserverocspresponse">CertOpenServerOcspResponse</a>.


## -returns



This function has no return value.




## -remarks



Each <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certopenserverocspresponse">CertOpenServerOcspResponse</a> and <b>CertAddRefServerOcspResponse</b> requires a corresponding <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcloseserverocspresponse">CertCloseServerOcspResponse</a>.



