---
UID: NF:xenroll.IEnroll.get_MyStoreTypeWStr
title: IEnroll::get_MyStoreTypeWStr
author: windows-sdk-content
description: Sets or retrieves the type of store specified by the MyStoreTypeWStr property.
old-location: security\ienroll4_mystoretypewstr.htm
tech.root: seccrypto
ms.assetid: 46f95ae3-efd2-4545-b31d-df04112aa737
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IEnroll interface [Security],MyStoreTypeWStr property, IEnroll.MyStoreTypeWStr, IEnroll.get_MyStoreTypeWStr, IEnroll::MyStoreTypeWStr, IEnroll::get_MyStoreTypeWStr, IEnroll::put_MyStoreTypeWStr, MyStoreTypeWStr property [Security], MyStoreTypeWStr property [Security],IEnroll interface, get_MyStoreTypeWStr, security.ienroll4_mystoretypewstr, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/IEnroll::MyStoreTypeWStr, xenroll/IEnroll::get_MyStoreTypeWStr, xenroll/IEnroll::put_MyStoreTypeWStr
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
 - IEnroll.MyStoreTypeWStr
 - IEnroll.get_MyStoreTypeWStr
 - IEnroll.put_MyStoreTypeWStr
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
- IEnroll.get_MyStoreTypeWStr
: 
---

# IEnroll::get_MyStoreTypeWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreTypeWStr</b> property sets or retrieves the type of store  specified by the 
<b>MyStoreTypeWStr</b> property.   This store type is passed directly on to <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>.

The default value for this property is sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>MyStoreTypeWStr</b> property affects the behavior of the following methods:

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
 

 

