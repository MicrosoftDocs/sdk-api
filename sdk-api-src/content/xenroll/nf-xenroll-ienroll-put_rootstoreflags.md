---
UID: NF:xenroll.IEnroll.put_RootStoreFlags
title: IEnroll::put_RootStoreFlags
author: windows-sdk-content
description: Sets or retrieves the registry location used for the root store.
old-location: security\ienroll4_rootstoreflags.htm
tech.root: SecCrypto
ms.assetid: fa4640db-f3e5-4fe0-a696-26b5e13b7dd1
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IEnroll interface [Security],RootStoreFlags property, IEnroll.RootStoreFlags, IEnroll.put_RootStoreFlags, IEnroll::RootStoreFlags, IEnroll::get_RootStoreFlags, IEnroll::put_RootStoreFlags, RootStoreFlags property [Security], RootStoreFlags property [Security],IEnroll interface, put_RootStoreFlags, security.ienroll4_rootstoreflags, xenroll/IEnroll::RootStoreFlags, xenroll/IEnroll::get_RootStoreFlags, xenroll/IEnroll::put_RootStoreFlags
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
 - IEnroll.RootStoreFlags
 - IEnroll.get_RootStoreFlags
 - IEnroll.put_RootStoreFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::put_RootStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreFlags</b> property sets or retrieves the registry location used for the root store.

The default value for  this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



The <b>RootStoreFlags</b> property value is passed to the 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> CryptoAPI function by using  its <i>dwFlags</i> parameter.


The <b>RootStoreFlags</b> property should be set before using the following methods:

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
 

 

