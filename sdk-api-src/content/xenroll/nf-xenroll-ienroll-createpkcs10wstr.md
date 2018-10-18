---
UID: NF:xenroll.IEnroll.createPKCS10WStr
title: IEnroll::createPKCS10WStr
author: windows-sdk-content
description: Creates a base64-encoded PKCS #10 certificate request.
old-location: security\ienroll4_createpkcs10wstr.htm
tech.root: seccrypto
ms.assetid: ebbcc9ad-9f87-4abe-963b-38c57a60e45e
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IEnroll interface [Security],createPKCS10WStr method, IEnroll.createPKCS10WStr, IEnroll::createPKCS10WStr, createPKCS10WStr, createPKCS10WStr method [Security], createPKCS10WStr method [Security],IEnroll interface, security.ienroll4_createpkcs10wstr, xenroll/IEnroll::createPKCS10WStr
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IEnroll.createPKCS10WStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::createPKCS10WStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createPKCS10WStr</b> method creates a base64-encoded PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

 This base64-encoded PKCS #10 certificate request (in <b>BSTR</b> form) can be submitted to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> to request  that a certificate be issued to the person or entity whose information it contains.


## -parameters




### -param DNName [in]

A null-terminated Unicode string that contains the distinguished name (DN) of the entity for which the request is being made. In this parameter, the DN name must follow the <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> naming convention. For example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) may be provided instead.


### -param Usage [in]

A null-terminated Unicode string that contains an OID that describes the purpose of the certificate being generated. For example, Individual or Commercial Authenticode certificate, or Client Authentication. You can also specify multiple OIDs separated by a comma.

The  OID is passed through to the PKCS #10 request. For general extensibility and ease of understanding, the control does not attempt to understand specific-purpose OIDs. Therefore if you specify a Client Authentication OID, the generated key will still be a signature key, not an <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange key</a>.


### -param pPkcs10Blob [out]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> that receives the base64-encoded PKCS10 certificate request.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



 If the method succeeds, the method returns S_OK and <i>pPkcs10Blob</i> contains a base64-encoded PKCS #10 request that can be directly posted to a web server for processing.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



By default, the Microsoft Base Cryptographic Provider is used, PROV_RSA_FULL is the provider type, a signature key is created, and a unique new key set is created.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

