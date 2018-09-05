---
UID: NF:xenroll.IEnroll.get_DeleteRequestCert
title: IEnroll::get_DeleteRequestCert
author: windows-sdk-content
description: The DeleteRequestCert property of IEnroll4 sets or retrieves a Boolean value that determines whether dummy certificates in the request store are deleted.
old-location: security\ienroll4_deleterequestcert.htm
old-project: seccrypto
ms.assetid: 54b85347-cdc1-42e3-bc26-0b50bd58131a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DeleteRequestCert property [Security], DeleteRequestCert property [Security],IEnroll interface, IEnroll interface [Security],DeleteRequestCert property, IEnroll.DeleteRequestCert, IEnroll.get_DeleteRequestCert, IEnroll::DeleteRequestCert, IEnroll::get_DeleteRequestCert, IEnroll::put_DeleteRequestCert, get_DeleteRequestCert, security.ienroll4_deleterequestcert, xenroll/IEnroll::DeleteRequestCert, xenroll/IEnroll::get_DeleteRequestCert, xenroll/IEnroll::put_DeleteRequestCert
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.redist: 
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
 - IEnroll.DeleteRequestCert
 - IEnroll.get_DeleteRequestCert
 - IEnroll.put_DeleteRequestCert
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::get_DeleteRequestCert


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>DeleteRequestCert</b> property sets or retrieves a Boolean value that  determines whether dummy certificates in the request store are deleted.

Dummy certificates are created for the purpose of persisting the keys generated for the PKCS #10 request during the enrollment process. The store specified by the 
<a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">RequestStoreNameWStr</a> property is where the dummy certificate is created. The newly generated keys are added as properties to the dummy certificate to persist them until a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> processes the request and responds with a PKCS #7. On acceptance of the PKCS #7, the dummy certificate is removed and the keys are added as properties of the issued certificate returned by the certification authority. For debugging and testing, it is often desirable to not delete the dummy certificate. Setting <b>DeleteRequestCert</b> to false prevents its deletion.

The default value for this property is  true. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>DeleteRequestCert</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

