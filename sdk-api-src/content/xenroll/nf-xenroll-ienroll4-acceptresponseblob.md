---
UID: NF:xenroll.IEnroll4.acceptResponseBlob
title: IEnroll4::acceptResponseBlob
author: windows-sdk-content
description: Accepts delivery of the credentials issued in response to an earlier call to createRequestWStr and places the credentials in the appropriate store.
old-location: security\ienroll4_acceptresponseblob.htm
tech.root: seccrypto
ms.assetid: 4a28bf6b-ad3d-414b-8740-ce7d4301a05b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IEnroll4 interface [Security],acceptResponseBlob method, IEnroll4.acceptResponseBlob, IEnroll4::acceptResponseBlob, acceptResponseBlob, acceptResponseBlob method [Security], acceptResponseBlob method [Security],IEnroll4 interface, security.ienroll4_acceptresponseblob, xenroll/IEnroll4::acceptResponseBlob
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
 - IEnroll4.acceptResponseBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll4::acceptResponseBlob


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptResponseBlob</b> method accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://msdn.microsoft.com/bc2b875c-96f8-453e-8f72-f9032d5aa773">createRequestWStr</a> and places the credentials in the appropriate store.

The response may be a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #7</a> format or a full <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) response. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param pblobResponse [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the response.


## -remarks



The response must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full CMC response; however, to accept a full CMC response, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> must support <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

