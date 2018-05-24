---
UID: NF:xenroll.IEnroll.freeRequestInfoBlob
title: IEnroll::freeRequestInfoBlob
author: windows-driver-content
description: The freeRequestInfoBlob method deletes a certificate context. This method was first defined in the IEnroll interface.
old-location: security\ienroll4_freerequestinfoblob.htm
old-project: SecCrypto
ms.assetid: 7c89de98-51b6-44c2-acd2-879d1d4e7f29
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IEnroll interface [Security],freeRequestInfoBlob method, IEnroll.freeRequestInfoBlob, IEnroll::freeRequestInfoBlob, freeRequestInfoBlob, freeRequestInfoBlob method [Security], freeRequestInfoBlob method [Security],IEnroll interface, security.ienroll4_freerequestinfoblob, xenroll/IEnroll::freeRequestInfoBlob
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	IEnroll.freeRequestInfoBlob
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::freeRequestInfoBlob


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>freeRequestInfoBlob</b> method deletes a certificate context. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param pkcs7OrPkcs10






#### - PKCS7OrPKCS10 [in]

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that specifies the session information whose context is being deleted.


## -returns




						The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

