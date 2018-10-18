---
UID: NF:xenroll.IEnroll2.InstallPKCS7Blob
title: IEnroll2::InstallPKCS7Blob
author: windows-sdk-content
description: Processes a certificate or chain of certificates, placing them into the appropriate certificate stores. This method differs from the acceptPKCS7Blob method in that InstallPKCS7Blob does not receive a request certificate.
old-location: security\ienroll4_installpkcs7blob.htm
tech.root: seccrypto
ms.assetid: fa704c5e-f6ec-4187-b787-7b15cc7d4eb4
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IEnroll2 interface [Security],InstallPKCS7Blob method, IEnroll2.InstallPKCS7Blob, IEnroll2::InstallPKCS7Blob, InstallPKCS7Blob, InstallPKCS7Blob method [Security], InstallPKCS7Blob method [Security],IEnroll2 interface, security.ienroll4_installpkcs7blob, xenroll/IEnroll2::InstallPKCS7Blob
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
 - IEnroll2.InstallPKCS7Blob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll2::InstallPKCS7Blob


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7Blob</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a>. This method differs from the  <a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a> method in that  <b>InstallPKCS7Blob</b> does not receive a request certificate. This method was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.


## -parameters




### -param pBlobPKCS7 [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains a certificate or chain of certificates.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll2</a>
 

 

