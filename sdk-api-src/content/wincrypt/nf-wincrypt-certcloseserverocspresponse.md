---
UID: NF:wincrypt.CertCloseServerOcspResponse
title: CertCloseServerOcspResponse function
author: windows-sdk-content
description: Closes an online certificate status protocol (OCSP) server response handle.
old-location: security\certcloseserverocspresponse.htm
tech.root: seccrypto
ms.assetid: 6247e8ca-ba12-432f-9bf8-a6c644f253e9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CertCloseServerOcspResponse, CertCloseServerOcspResponse function [Security], security.certcloseserverocspresponse, wincrypt/CertCloseServerOcspResponse
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
 - CertCloseServerOcspResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertCloseServerOcspResponse function


## -description


The <b>CertCloseServerOcspResponse</b> function closes an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) server response handle.


## -parameters




### -param hServerOcspResponse [in]

The handle to close for an OCSP server response.


### -param dwFlags [in]

This parameter is not used and must be zero.


## -returns



This function does not return a value.




## -remarks



The <b>CertCloseServerOcspResponse</b> function closes a handle returned by either the <a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a> or <a href="https://msdn.microsoft.com/6ccc0e85-1fa0-480c-a5b4-b21ba811e5d0">CertAddRefServerOcspResponse</a> function.




## -see-also




<a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a>
 

 

