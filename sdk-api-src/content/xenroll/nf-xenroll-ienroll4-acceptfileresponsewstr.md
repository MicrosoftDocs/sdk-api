---
UID: NF:xenroll.IEnroll4.acceptFileResponseWStr
title: IEnroll4::acceptFileResponseWStr
author: windows-sdk-content
description: Accepts delivery of the credentials issued in response to an earlier call to createFileRequestWStr, and it places the credentials in the appropriate store.
old-location: security\ienroll4_acceptfileresponsewstr.htm
tech.root: seccrypto
ms.assetid: b9c92f20-5f23-4dda-9e80-df9bf400ac08
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IEnroll4 interface [Security],acceptFileResponseWStr method, IEnroll4.acceptFileResponseWStr, IEnroll4::acceptFileResponseWStr, acceptFileResponseWStr, acceptFileResponseWStr method [Security], acceptFileResponseWStr method [Security],IEnroll4 interface, security.ienroll4_acceptfileresponsewstr, xenroll/IEnroll4::acceptFileResponseWStr
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
 - IEnroll4.acceptFileResponseWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xenroll.h
: 
- IEnroll4.acceptFileResponseWStr
: 
---

# IEnroll4::acceptFileResponseWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFileResponseWStr</b> method accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://msdn.microsoft.com/5750f2ad-a96f-4bc7-9a1f-354e279a7860">createFileRequestWStr</a>, and it places the credentials in the appropriate store.

The response may be a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #7</a> message or a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) response. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param pwszResponseFileName [in]

A pointer to a null-terminated wide character string that represents the name of the file that contains the response.


## -remarks



The response named in the <i>pwszResponseFileName</i> parameter must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full CMC response; however, to accept a full CMC response, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> must support <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

