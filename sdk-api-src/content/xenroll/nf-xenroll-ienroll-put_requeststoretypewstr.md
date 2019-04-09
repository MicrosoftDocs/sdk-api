---
UID: NF:xenroll.IEnroll.put_RequestStoreTypeWStr
title: IEnroll::put_RequestStoreTypeWStr (xenroll.h)
author: windows-sdk-content
description: Sets or retrieves the type of store to use for the store specified by the RequestStoreNameWStr property. This store type is passed directly to the CertOpenStore function.
old-location: security\ienroll4_requeststoretypewstr.htm
tech.root: SecCrypto
ms.assetid: 5b06552a-7b8d-4044-9c2c-994f67e9c36d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],RequestStoreTypeWStr property, IEnroll.RequestStoreTypeWStr, IEnroll.put_RequestStoreTypeWStr, IEnroll4 interface [Security],RequestStoreTypeWStr property, IEnroll4.RequestStoreTypeWStr, IEnroll4::get_RequestStoreTypeWStr, IEnroll4::put_RequestStoreTypeWStr, IEnroll::RequestStoreTypeWStr, IEnroll::get_RequestStoreTypeWStr, IEnroll::put_RequestStoreTypeWStr, RequestStoreTypeWStr property [Security], RequestStoreTypeWStr property [Security],IEnroll interface, RequestStoreTypeWStr property [Security],IEnroll4 interface, get_RequestStoreTypeWStr, put_RequestStoreTypeWStr, security.ienroll4_requeststoretypewstr, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/IEnroll4::RequestStoreTypeWStr, xenroll/IEnroll4::get_RequestStoreTypeWStr, xenroll/IEnroll4::put_RequestStoreTypeWStr, xenroll/IEnroll::RequestStoreTypeWStr, xenroll/IEnroll::get_RequestStoreTypeWStr, xenroll/IEnroll::put_RequestStoreTypeWStr
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
 - IEnroll.RequestStoreTypeWStr
 - IEnroll.get_RequestStoreTypeWStr
 - IEnroll.put_RequestStoreTypeWStr
 - IEnroll4.RequestStoreTypeWStr
 - IEnroll4.get_RequestStoreTypeWStr
 - IEnroll4.put_RequestStoreTypeWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::put_RequestStoreTypeWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreTypeWStr</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">RequestStoreNameWStr</a> property. This store type is passed directly  to the <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function.

The default value of  this property is sz_CERT_STORE_PROV_SYSTEM. If the default is not to be used, this property must be set to the same value before calls to 
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a> and 
				<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a> and again before calls to 
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a> and 
				<a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>.

Only system stores are supported. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



Typically, modification of the <b>RequestStoreTypeWStr</b> property is  performed only in advanced applications.


<b>RequestStoreTypeWStr</b> affects the behavior of the following methods:

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
 

 

