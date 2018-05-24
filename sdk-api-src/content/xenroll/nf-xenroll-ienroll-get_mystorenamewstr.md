---
UID: NF:xenroll.IEnroll.get_MyStoreNameWStr
title: IEnroll::get_MyStoreNameWStr
author: windows-driver-content
description: The MyStoreNameWStr property of IEnroll4 sets or retrieves the name of the store where certificates with linked private keys are kept.
old-location: security\ienroll4_mystorenamewstr.htm
old-project: SecCrypto
ms.assetid: 077bc593-0071-4f41-8d07-141c9959b6ed
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IEnroll interface [Security],MyStoreNameWStr property, IEnroll.MyStoreNameWStr, IEnroll.get_MyStoreNameWStr, IEnroll::MyStoreNameWStr, IEnroll::get_MyStoreNameWStr, IEnroll::put_MyStoreNameWStr, MyStoreNameWStr property [Security], MyStoreNameWStr property [Security],IEnroll interface, get_MyStoreNameWStr, security.ienroll4_mystorenamewstr, xenroll/IEnroll::MyStoreNameWStr, xenroll/IEnroll::get_MyStoreNameWStr, xenroll/IEnroll::put_MyStoreNameWStr
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
-	IEnroll.MyStoreNameWStr
-	IEnroll.get_MyStoreNameWStr
-	IEnroll.put_MyStoreNameWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::get_MyStoreNameWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreNameWStr</b> property  sets or retrieves the name of the store  where certificates with linked <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private keys</a> are kept.

The value of <b>MyStoreNameWStr</b> specifies the store in which to place the new certificate produced from 
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a> or 
<a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>. The default value for this property is "MY". This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>MyStoreNameWStr</b> property affects the behavior of the following methods:

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
 

 

