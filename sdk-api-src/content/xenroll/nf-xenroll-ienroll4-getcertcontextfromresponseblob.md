---
UID: NF:xenroll.IEnroll4.getCertContextFromResponseBlob
title: IEnroll4::getCertContextFromResponseBlob
author: windows-sdk-content
description: Retrieves the certificate from a certification authority's response.
old-location: security\ienroll4_getcertcontextfromresponseblob.htm
tech.root: seccrypto
ms.assetid: 824626bf-a20d-4d34-a061-9f54b142e0fc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnroll4 interface [Security],getCertContextFromResponseBlob method, IEnroll4.getCertContextFromResponseBlob, IEnroll4::getCertContextFromResponseBlob, getCertContextFromResponseBlob, getCertContextFromResponseBlob method [Security], getCertContextFromResponseBlob method [Security],IEnroll4 interface, security.ienroll4_getcertcontextfromresponseblob, xenroll/IEnroll4::getCertContextFromResponseBlob
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
 - IEnroll4.getCertContextFromResponseBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll4::getCertContextFromResponseBlob


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertContextFromResponseBlob</b> method retrieves the certificate from a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority's</a> response.This method was first defined by the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param pblobResponse [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the response.


### -param ppCertContext [out]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure  that receives the certificate retrieved from the response.


## -remarks



The response contained in <i>pblobResponse</i> must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) response. However, to accept a full CMC response, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> must support <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

