---
UID: NF:xenroll.IEnroll4.InstallPKCS7BlobEx
title: IEnroll4::InstallPKCS7BlobEx
author: windows-sdk-content
description: The same as InstallPKCS7Blob except that it returns the number of certificates actually installed in local stores.
old-location: security\ienroll4_installpkcs7blobex.htm
old-project: seccrypto
ms.assetid: 6a65eac6-3fe5-4464-876d-80eedaca7ae6
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IEnroll4 interface [Security],InstallPKCS7BlobEx method, IEnroll4.InstallPKCS7BlobEx, IEnroll4::InstallPKCS7BlobEx, InstallPKCS7BlobEx, InstallPKCS7BlobEx method [Security], InstallPKCS7BlobEx method [Security],IEnroll4 interface, security.ienroll4_installpkcs7blobex, xenroll/IEnroll4::InstallPKCS7BlobEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.InstallPKCS7BlobEx
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::InstallPKCS7BlobEx


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7BlobEx</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a>. The <b>InstallPKCS7BlobEx</b> method is the same as 
<a href="https://msdn.microsoft.com/fa704c5e-f6ec-4187-b787-7b15cc7d4eb4">InstallPKCS7Blob</a> except that it returns the number of certificates actually installed in local stores.


## -parameters




### -param pBlobPKCS7 [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains a certificate or chain of certificates.


### -param plCertInstalled [out]

Returns the number of certificates installed into local stores.


## -returns




						 The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

