---
UID: NF:xenroll.IEnroll.get_CAStoreTypeWStr
title: IEnroll::get_CAStoreTypeWStr
author: windows-sdk-content
description: Sets or retrieves the type of store to use for the store specified by the CAStoreNameWStr property.
old-location: security\ienroll4_castoretypewstr.htm
tech.root: seccrypto
ms.assetid: cbb60c1c-04ed-4477-bf8e-4dae9fd964ef
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CAStoreTypeWStr property [Security], CAStoreTypeWStr property [Security],IEnroll interface, IEnroll interface [Security],CAStoreTypeWStr property, IEnroll.CAStoreTypeWStr, IEnroll.get_CAStoreTypeWStr, IEnroll::CAStoreTypeWStr, IEnroll::get_CAStoreTypeWStr, IEnroll::put_CAStoreTypeWStr, get_CAStoreTypeWStr, security.ienroll4_castoretypewstr, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/IEnroll::CAStoreTypeWStr, xenroll/IEnroll::get_CAStoreTypeWStr, xenroll/IEnroll::put_CAStoreTypeWStr
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
 - IEnroll.CAStoreTypeWStr
 - IEnroll.get_CAStoreTypeWStr
 - IEnroll.put_CAStoreTypeWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::get_CAStoreTypeWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreTypeWStr</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">CAStoreNameWStr</a> property. This store type is passed directly on to the  <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function.

The default value for this property is  sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>CAStoreTypeWStr</b> property affects the behavior of the following methods:

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
 

 

