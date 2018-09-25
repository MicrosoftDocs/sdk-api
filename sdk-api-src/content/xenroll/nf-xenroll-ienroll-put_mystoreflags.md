---
UID: NF:xenroll.IEnroll.put_MyStoreFlags
title: IEnroll::put_MyStoreFlags
author: windows-sdk-content
description: Sets or retrieves the registry location used for the MY store.
old-location: security\ienroll4_mystoreflags.htm
tech.root: seccrypto
ms.assetid: e545920a-0c39-49bb-90cc-87039d2e2cfd
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IEnroll interface [Security],MyStoreFlags property, IEnroll.MyStoreFlags, IEnroll.put_MyStoreFlags, IEnroll::MyStoreFlags, IEnroll::get_MyStoreFlags, IEnroll::put_MyStoreFlags, MyStoreFlags property [Security], MyStoreFlags property [Security],IEnroll interface, put_MyStoreFlags, security.ienroll4_mystoreflags, xenroll/IEnroll::MyStoreFlags, xenroll/IEnroll::get_MyStoreFlags, xenroll/IEnroll::put_MyStoreFlags
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
 - IEnroll.MyStoreFlags
 - IEnroll.get_MyStoreFlags
 - IEnroll.put_MyStoreFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::put_MyStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreFlags</b> property sets or retrieves the registry location used for the MY store.

The default value for  this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



The <b>MyStoreFlags</b> property value is passed to the 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> CryptoAPI function by using its <i>dwFlags</i> parameter.


The <b>MyStoreFlags</b> property should be set before using the following methods:

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
 

 

