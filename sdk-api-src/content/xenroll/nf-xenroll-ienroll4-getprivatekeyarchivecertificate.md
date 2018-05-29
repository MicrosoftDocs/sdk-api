---
UID: NF:xenroll.IEnroll4.GetPrivateKeyArchiveCertificate
title: IEnroll4::GetPrivateKeyArchiveCertificate
author: windows-sdk-content
description: The GetPrivateKeyArchiveCertificate method retrieves the certificate used to archive the private key. This method was first defined in the IEnroll4 interface.
old-location: security\ienroll4_getprivatekeyarchivecertificate.htm
old-project: SecCrypto
ms.assetid: 0fdcd4ff-2dd1-4654-9901-a9824d4eddec
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetPrivateKeyArchiveCertificate, GetPrivateKeyArchiveCertificate method [Security], GetPrivateKeyArchiveCertificate method [Security],IEnroll4 interface, IEnroll4 interface [Security],GetPrivateKeyArchiveCertificate method, IEnroll4.GetPrivateKeyArchiveCertificate, IEnroll4::GetPrivateKeyArchiveCertificate, security.ienroll4_getprivatekeyarchivecertificate, xenroll/IEnroll4::GetPrivateKeyArchiveCertificate
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	IEnroll4.GetPrivateKeyArchiveCertificate
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::GetPrivateKeyArchiveCertificate


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetPrivateKeyArchiveCertificate</b> method retrieves the certificate used to archive the private key. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters






## -returns



Pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that represents the certificate used to archive the private key, or <b>NULL</b> if an error is encountered.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

