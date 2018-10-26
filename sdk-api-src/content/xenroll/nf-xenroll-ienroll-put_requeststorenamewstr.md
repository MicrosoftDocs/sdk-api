---
UID: NF:xenroll.IEnroll.put_RequestStoreNameWStr
title: IEnroll::put_RequestStoreNameWStr
author: windows-sdk-content
description: The RequestStoreNameWStr property of IEnroll4 sets or retrieves the name of the store that contains the dummy certificate.
old-location: security\ienroll4_requeststorenamewstr.htm
tech.root: seccrypto
ms.assetid: 4ad739c0-fcf7-435b-b427-96ecca1afab7
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IEnroll interface [Security],RequestStoreNameWStr property, IEnroll.RequestStoreNameWStr, IEnroll.put_RequestStoreNameWStr, IEnroll4 interface [Security],RequestStoreNameWStr property, IEnroll4.RequestStoreNameWStr, IEnroll4::get_RequestStoreNameWStr, IEnroll4::put_RequestStoreNameWStr, IEnroll::RequestStoreNameWStr, IEnroll::get_RequestStoreNameWStr, IEnroll::put_RequestStoreNameWStr, RequestStoreNameWStr property [Security], RequestStoreNameWStr property [Security],IEnroll interface, RequestStoreNameWStr property [Security],IEnroll4 interface, get_RequestStoreNameWStr, put_RequestStoreNameWStr, security.ienroll4_requeststorenamewstr, xenroll/IEnroll4::RequestStoreNameWStr, xenroll/IEnroll4::get_RequestStoreNameWStr, xenroll/IEnroll4::put_RequestStoreNameWStr, xenroll/IEnroll::RequestStoreNameWStr, xenroll/IEnroll::get_RequestStoreNameWStr, xenroll/IEnroll::put_RequestStoreNameWStr
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
 - IEnroll.RequestStoreNameWStr
 - IEnroll.get_RequestStoreNameWStr
 - IEnroll.put_RequestStoreNameWStr
 - IEnroll4.RequestStoreNameWStr
 - IEnroll4.get_RequestStoreNameWStr
 - IEnroll4.put_RequestStoreNameWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::put_RequestStoreNameWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreNameWStr</b> property sets or retrieves the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> processes the request and responds with a PKCS #7.

The default value for this property is  "REQUEST". If the default is not to be used, this property must be set to the store to be used before calls to 
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a><b>/</b><a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a> and again before calls to 
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a><b>/</b><a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>.

This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



Typically, modification of the <b>RequestStoreNameWStr</b> property is  performed only in advanced applications. Changing this value is not recommended for most applications.


The <b>RequestStoreNameWStr</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

