---
UID: NF:xenroll.IEnroll4.SetPrivateKeyArchiveCertificate
title: IEnroll4::SetPrivateKeyArchiveCertificate
author: windows-sdk-content
description: The SetPrivateKeyArchiveCertificate method specifies the certificate used to archive the private key. This method was first defined in the IEnroll4 interface.
old-location: security\ienroll4_setprivatekeyarchivecertificate.htm
old-project: SecCrypto
ms.assetid: e37a8055-4074-425b-8f88-69b898855824
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEnroll4 interface [Security],SetPrivateKeyArchiveCertificate method, IEnroll4.SetPrivateKeyArchiveCertificate, IEnroll4::SetPrivateKeyArchiveCertificate, SetPrivateKeyArchiveCertificate, SetPrivateKeyArchiveCertificate method [Security], SetPrivateKeyArchiveCertificate method [Security],IEnroll4 interface, security.ienroll4_setprivatekeyarchivecertificate, xenroll/IEnroll4::SetPrivateKeyArchiveCertificate
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
 - IEnroll4.SetPrivateKeyArchiveCertificate
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::SetPrivateKeyArchiveCertificate


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SetPrivateKeyArchiveCertificate</b> method specifies the certificate used to archive the private key. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param pPrivateKeyArchiveCert [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that specifies the certificate used to archive the private key.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

