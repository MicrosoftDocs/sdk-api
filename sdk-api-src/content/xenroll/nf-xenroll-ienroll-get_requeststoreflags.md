---
UID: NF:xenroll.IEnroll.get_RequestStoreFlags
title: IEnroll::get_RequestStoreFlags
author: windows-sdk-content
description: The RequestStoreFlags property of IEnroll4 sets or retrieves the registry location used for the request store.
old-location: security\ienroll4_requeststoreflags.htm
old-project: seccrypto
ms.assetid: 95ed42ed-04ff-482c-954c-a6c9dd9ccd4c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnroll interface [Security],RequestStoreFlags property, IEnroll.RequestStoreFlags, IEnroll.get_RequestStoreFlags, IEnroll::RequestStoreFlags, IEnroll::get_RequestStoreFlags, IEnroll::put_RequestStoreFlags, RequestStoreFlags property [Security], RequestStoreFlags property [Security],IEnroll interface, get_RequestStoreFlags, security.ienroll4_requeststoreflags, xenroll/IEnroll::RequestStoreFlags, xenroll/IEnroll::get_RequestStoreFlags, xenroll/IEnroll::put_RequestStoreFlags
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
 - IEnroll.RequestStoreFlags
 - IEnroll.get_RequestStoreFlags
 - IEnroll.put_RequestStoreFlags
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::get_RequestStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreFlags</b> property sets or retrieves the registry location used for the request store.

 The default value for this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



The <b>RequestStoreFlags</b> property value is passed to the 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> CryptoAPI function  by using its <i>dwFlags</i> parameter.

Typically, modification of the <b>RequestStoreFlags</b> property is  performed only in advanced applications.


The <b>RequestStoreFlags</b> property should be set before using the following methods:

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




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

