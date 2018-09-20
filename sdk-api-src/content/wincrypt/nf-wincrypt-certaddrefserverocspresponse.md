---
UID: NF:wincrypt.CertAddRefServerOcspResponse
title: CertAddRefServerOcspResponse function
author: windows-sdk-content
description: Increments the reference count for an HCERT_SERVER_OCSP_RESPONSE handle.
old-location: security\certaddrefserverocspresponse.htm
tech.root: seccrypto
ms.assetid: 6ccc0e85-1fa0-480c-a5b4-b21ba811e5d0
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CertAddRefServerOcspResponse, CertAddRefServerOcspResponse function [Security], security.certaddrefserverocspresponse, wincrypt/CertAddRefServerOcspResponse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
---

# CertAddRefServerOcspResponse function


## -description


The <b>CertAddRefServerOcspResponse</b> function increments the reference count for an <b>HCERT_SERVER_OCSP_RESPONSE</b> handle.


## -parameters




### -param hServerOcspResponse [in]

A handle to an <b>HCERT_SERVER_OCSP_RESPONSE</b> returned by <a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a>.


## -returns



This function has no return value.




## -remarks



Each <a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a> and <b>CertAddRefServerOcspResponse</b> requires a corresponding <a href="https://msdn.microsoft.com/6247e8ca-ba12-432f-9bf8-a6c644f253e9">CertCloseServerOcspResponse</a>.



