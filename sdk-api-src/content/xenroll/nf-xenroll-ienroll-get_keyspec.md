---
UID: NF:xenroll.IEnroll.get_KeySpec
title: IEnroll::get_KeySpec (xenroll.h)
author: windows-sdk-content
description: Sets or retrieves the type of key generated.
old-location: security\ienroll4_keyspec.htm
tech.root: SecCrypto
ms.assetid: b05851a0-6228-44e4-9bd7-354c862596e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],KeySpec property, IEnroll.KeySpec, IEnroll.get_KeySpec, IEnroll::KeySpec, IEnroll::get_KeySpec, IEnroll::put_KeySpec, KeySpec property [Security], KeySpec property [Security],IEnroll interface, get_KeySpec, security.ienroll4_keyspec, xenroll/IEnroll::KeySpec, xenroll/IEnroll::get_KeySpec, xenroll/IEnroll::put_KeySpec
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
 - IEnroll.KeySpec
 - IEnroll.get_KeySpec
 - IEnroll.put_KeySpec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::get_KeySpec


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>KeySpec</b> property sets or retrieves the  type of key generated.

 Valid values are determined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in use. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



For the Microsoft Base Cryptographic Provider, the <b>KeySpec</b> property has a value of AT_KEYEXCHANGE for <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a>, or AT_SIGNATURE for signature keys. The default is AT_SIGNATURE.

For information about the other Microsoft CSPs, see 
<a href="https://msdn.microsoft.com/4e6eb2df-a917-4533-b9f1-8da39598d0b8">Cryptographic Service Providers</a> in the CryptoAPI 2.0 documentation.

For information about other CSPs, see the documentation provided with the CSP.


The <b>KeySpec</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

