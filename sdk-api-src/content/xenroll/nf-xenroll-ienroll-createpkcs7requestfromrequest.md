---
UID: NF:xenroll.IEnroll.CreatePKCS7RequestFromRequest
title: IEnroll::CreatePKCS7RequestFromRequest (xenroll.h)
author: windows-sdk-content
description: The CreatePKCS7RequestFromRequest method creates a PKCS #7 request from an existing certificate request. This method was first defined in the IEnroll interface.
old-location: security\ienroll4_createpkcs7requestfromrequest.htm
tech.root: SecCrypto
ms.assetid: f1d2df72-bedc-45e5-8c0a-a731845d4487
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreatePKCS7RequestFromRequest, CreatePKCS7RequestFromRequest method [Security], CreatePKCS7RequestFromRequest method [Security],IEnroll interface, CreatePKCS7RequestFromRequest method [Security],IEnroll2 interface, IEnroll interface [Security],CreatePKCS7RequestFromRequest method, IEnroll.CreatePKCS7RequestFromRequest, IEnroll2 interface [Security],CreatePKCS7RequestFromRequest method, IEnroll2::CreatePKCS7RequestFromRequest, IEnroll::CreatePKCS7RequestFromRequest, security.ienroll4_createpkcs7requestfromrequest, xenroll/IEnroll2::CreatePKCS7RequestFromRequest, xenroll/IEnroll::CreatePKCS7RequestFromRequest
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.CreatePKCS7RequestFromRequest
 - IEnroll2.CreatePKCS7RequestFromRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::CreatePKCS7RequestFromRequest


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CreatePKCS7RequestFromRequest</b> method creates a PKCS #7 request from an existing certificate request. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param pRequest [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the existing request.


### -param pSigningCertContext [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that represents the certificate used to sign the request.


### -param pPkcs7Blob [out]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that receives the returned PKCS  #7 certificate request.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll2</a>
 

 

